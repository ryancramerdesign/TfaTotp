# TOTP Two Factor Authentication for ProcessWire

TOTP means Time-based One-Time Password algorithm, which is a standard used by many
2FA authenticator apps such as the following (all available on both Android and iOS):

- Google Authenticator
- Authy Authenticator by Twilio
- Microsoft Authenticator
- LastPass Authenticator
- And several others…

### Requirements  

- ProcessWire 3.0.109 or newer. 
- PHP 5.6 or newer. 
- For users wanting to enable 2FA, it requires that they have a TOTP 
  authenticator app installed, typically on a mobile phone. 

### How to install 

1. Place the files for this module in `/site/modules/TfaTotp/`.
2. In the admin, go to Modules > Refresh.
3. Go to Modules > Site > Tfa, and click “Install” for this module.  

### How to use

1. Edit your user profile in the ProcessWire admin.
2. Scroll to the bottom and you should see a new field for “Two factor authentication”. 
3. Select the “TOTP” option and click Submit (note: it’ll ask for your password first). 
4. After submitting the change, go back to the field and it will want you to open your 
   authenticator application to scan the QR code it provides.
5. After scanning the QR code, your authenticator app will provide a 6 digit code for 
   you to enter in ProcessWire. This is just to confirm that everything is working. 
   After doing this, click submit, and you are done. 

Once two-factor authentication is enabled, when you login, there will be a second step
where it will ask you to enter a code. You can get this code by opening your chosen 
authenticator app.

### Credits

- [TwoFactorAuth TOTP library](https://github.com/RobThree/TwoFactorAuth) 
  by [RobThree](https://github.com/RobThree) (license: MIT)
- [QR Code Generator library](https://github.com/kazuhikoarase/qrcode-generator) 
  by [Kazuhiko Arase](https://github.com/kazuhikoarase) (license: MIT)
- [TfaTotp ProcessWire module](https://github.com/ryancramerdesign/TfaTotp) 
  by [Ryan Cramer](https://github.com/ryancramerdesign/) (license: MIT or MPL 2)
  

