# jquery-validate-plugin
jquery-validate-plugin

https://stackoverflow.com/questions/31518779/how-to-install-jquery-validate-plugin

//--------------------------------
https://stackoverflow.com/questions/16660900/webforms-unobtrusivevalidationmode-requires-a-scriptresourcemapping-for-jquery

Step 1.
Put the jquery.validate.js file in your project from this link:
https://jqueryvalidation.org/ 

Step 2.
In the Customers.aspx page, paste in the link to the jquery file:
<!-- Adding Client-Side jQuery Validation -->
<script src="jquery.validate.js"></script>
.
.
Step 3. Paste in the web config file:
<appSettings>
      <add key="ValidationSettings:UnobtrusiveValidationMode" value="None" />
</appSettings>

Step 4. 
Link the text box class ID to the RequiredFieldValidator:

<!-- --------- RequiredFieldValidator ------------ -->
<asp:RequiredFieldValidator ID="RequiredFieldValidatortxtName" runat="server" Display="Dynamic" 
ForeColor="Red" ErrorMessage="Name is required" SetFocusOnError="True" ControlToValidate="txtName"></asp:RequiredFieldValidator>
