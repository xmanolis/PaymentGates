This plugin enables viva payments via Redirection method in Opencart 3.0. 
It is based on the viva plugin for Opencart 2.3, just adjusted for the new version of Opencart: https://github.com/VivaPayments/API/tree/master/Plugins/opencart/Opencart%202.3
The same instructions apply here as well therefore.

----
To connect the plugin with your e-commerce platform and Vivawallet you would have to create a new Payment Source in your Vivawallet business account.
You can create the new Payment Source from the menu My Sales - Payment Sources - New Website/App.
Code - use this code in your plugin
Source Name - provide a logic name here
Linked Wallet - link the payment source to the wallet you want to use with it
Protocol - in case your e-commerce platform uses SSL on the checkout select https, otherwise use https
Integration method - redirection
Company Logo - your png company logo to display on the Vivawallet payment page
Success URL - index.php?route=extension/payment/vivawallet/callback&success
Failure URL - index.php?route=extension/payment/vivawallet/callback&fail
Advanced Configuration - usually no need to make any changes here

Wait until Vivawallet has activated your newly created Payment Source before activating the plugin in your e-commerce platform.

INSTALLATION of the plugin:
1a) Extract the vivawallet.ocmod.zip and upload the files from the upload directory to their corresponding location on the server with ftp/ssh.
1b) Or use the extension installer, click the Upload button and select the vivawallet.ocmod.zip package.
2. Overwrite files/folders as necessary (no core opencart files will be overwritten)
3. Login to the Open Cart admin section and go to Extensions > Payments (from dropdown)
4. Find Vivawallet in the list of extensions
5. Click "Install" and then "Edit" the payment module settings:
Merchant ID, API Key: You can find your Merchant ID and API Key when you login your business account under Settings - API Access.
Source Code: taken by the Payment Source you created 
OrderCode URL: if you are using the demo version, then: http://demo.vivapayments.com/api/orders
Redirect URL: if you are using the demo version, then: http://demo.vivapayments.com/web/newtransaction.aspx
