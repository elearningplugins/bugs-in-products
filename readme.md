After a random refresh, there's a captcha message:

<img width="1454" height="1801" alt="image" src="https://github.com/user-attachments/assets/b7d37541-2320-4ca7-ae6c-a561928140e3" />

<img width="1746" height="1126" alt="image" src="https://github.com/user-attachments/assets/dd32a526-6ed4-44c5-985c-7c47c0e9cdb3" />

Per Google Chrome analysis:

This network request to https://www.google.com/recaptcha/enterprise/pat is likely part of the reCAPTCHA Enterprise verification process. The pat endpoint is typically used for generating or validating user tokens as part of the bot detection mechanism.

The key issue here is the 401 Unauthorized status code. This indicates that the request lacked valid authentication credentials for the target resource. In the context of reCAPTCHA, this most likely means that:

The provided reCAPTCHA key (k=6LcIy_MqAAAAAMKiupFSbmzW3xjGSlIfRzNWYMjC) is invalid or has expired.
The request is missing required authentication parameters or the format of the request payload (which is application/x-protobuffer) is incorrect.
There's a configuration issue with your reCAPTCHA Enterprise setup.
