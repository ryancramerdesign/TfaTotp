# ProcessWire Two Factor Authentication

## Time-based One-Time Password algorithm (TOTP)

Works with apps that use TOTP, like:

- Google Authenticator
- Authy
- Microsoft Authenticator
- Numerous others

This module implements ProcessWire’s Tfa module interface and uses 
the [TwoFactorAuth library](https://github.com/RobThree/TwoFactorAuth) by [RobThree](https://github.com/RobThree). 

Requires ProcessWire 3.0.109 or newer. Also requires that you have an authenticator 
application installed on your mobile device. 

### How to install 

1. Place the files for this module in /site/modules/TfaTotp/
2. In the admin, go to Modules > Refresh.
3. Go to Modules > Site > Tfa, and click install for this module.  

### How to setup two-factor authentication

1. Edit your user profile in the ProcessWire admin.
2. Scroll to the bottom and you should see a new field for “Two factor authentication”. 
3. Select the “TOTP” option and click Submit (note: it’ll ask for your password first). 
4. After submitting the change, go back to the field and it will want you to open your 
   authenticator application to scan the QR code it provides.
5. After scanning the QR code, your authenticator app will provide a 6 digit code for 
   you to enter in ProcessWire. This is just to confirm that everything is working. 
   After doing this, and hitting submit, you are done. 

Once two-factor authentication is enabled, when you login, there will be a second step
where it will ask you to enter a code. You can get this code by opening your authenticator 
app.
