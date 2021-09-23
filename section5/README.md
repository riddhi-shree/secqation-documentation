# DVWA: Get Your Hands Dirty

Damn Vulnerable Web App (DVWA) is a PHP/MySQL web application that is damn vulnerable. Let's solve [DVWA](https://dvwa.co.uk/).

## DVWA Setup

1. Start your own vulnerable instance of DVWA

    ```bash
    docker run --rm -it -p 80:80 vulnerables/web-dvwa
    ```

2. Add following line in the `/etc/hosts` file

    ```
    127.0.1.1	secqation
    ```

3. Go to http://secqation/login.php

    ![DVWA](images/dvwa.png)

4. Start hacking.

## Be Lazy. But Don't Be  Boring.

Let's make hacking DVWA a bit more interesting...



## References:

* https://github.com/digininja/DVWA
