# codeigniter_bootstrap_alert
This tiny helper function helps you output normal php session flash data in a bootstrap alert dialog
This helper function 
Requires:
 <b>Codeigniter</b>
 <b>Bootstrap</b>
There are just two methods in this helper:
 1. doBootstrapAlert($message, $alertType)
 2. echoBootstrapAlert()
 
function doBoostrapAlert takes two arguments:
 - $message: the message to be displayed in the alert dialog. It can contain html tags like <strong></strong> etc.
 - $alertType: the value of the alert dialog type. This determines the color of the alert dialog
     e.g success -> green
         warning -> yellow
         danger -> red
         primary -> deep blue
         info -> light blue
         

To use this helper, clone or download this file into your localhost, 
copy the utilities_helper.php file into applications/helper folder of your project.
Load the helper into your controller, by using $this->load->helper("utilities_helper") in the constructor or within any controller where you want to use the helper,
OR by autoloading it in config/autoload.php file
$autoload['helper'] = array('utilities_helper');

In your controller, invoke the method doBootstrapAlert($message, $alertType);
e.g doBootstrapAlert("Your account has been successfully credited", "success");
then, in your view file, call the echoBootstrapAlert() method
And that's it.

Note that, since the idea of flash data is being implemented, if you refresh the page after the alert dialog will disappear.
