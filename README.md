# WirePHPMailer

This module using [PHPMailer 6.0.3](https://github.com/PHPMailer/PHPMailer). You can see an example usage below.

[Simple example](https://github.com/PHPMailer/PHPMailer#a-simple-example)

[Other examples](https://github.com/PHPMailer/PHPMailer/tree/master/examples)

[Wiki](https://github.com/PHPMailer/PHPMailer/wiki)

You can set your configs from module settings or you can directly call `$mail = wire("modules")->get("WirePHPMailer"); $mail = $mail->mailer();` function for `new PHPMailer()` instance.

### Module usage :

```php
$mail = wire("modules")->get("WirePHPMailer");
$mail = $mail->mailer();
$mail->addAddress("email@domain.ltd", "Someone");
$mail->isHTML(true);
$mail->Subject = "WirePHPMailer";
$html = "<h1>WirePHPMailer</h1>";
$text = "WirePHPMailer";
$mail->Body    = $html;
$mail->AltBody = $text;
$mail->send();
```