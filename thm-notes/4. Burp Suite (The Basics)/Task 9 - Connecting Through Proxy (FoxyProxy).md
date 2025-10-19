
### What is a proxy?
- Proxy server is a system or router than acts as an intermediary between a client and web server.
- Proxy can intercept requests, then decide what to do with them

1. **Install FoxyProxy:** Download and install the [FoxyProxy Basic extension](https://addons.mozilla.org/en-US/firefox/addon/foxyproxy-basic/).
    **Note: FoxyProxy is already installed on the AttackBox.**
2. **Access FoxyProxy Options:** Once installed, a button will appear at the top right of the Firefox browser. Click on the FoxyProxy button to access the FoxyProxy options pop-up.
    
    ![](https://tryhackme-images.s3.amazonaws.com/user-uploads/5d9e176315f8850e719252ed/room-content/fee3f150ebb4d9301023188fddc0458a.png)
    
3. **Create Burp Proxy Configuration:** In the FoxyProxy options pop-up, click the **Options** button. This will open a new browser tab with the FoxyProxy configurations. Click the **Add** button to create a new proxy configuration.
    
    ![](https://tryhackme-images.s3.amazonaws.com/user-uploads/5d9e176315f8850e719252ed/room-content/5a73425b5de3395c5db2962b9d613506.png)
    
4. **Add Proxy Details:** On the "Add Proxy" page, fill in the following values:
    
    - Title: `Burp` (or any preferred name)
    - Proxy IP: `127.0.0.1`
    - Port: `8080`
    
      ![](https://tryhackme-images.s3.amazonaws.com/user-uploads/5d9e176315f8850e719252ed/room-content/b2d6f2b724f123070ca434bf2759df91.png)
    
5. **Save Configuration:** Click **Save** to save the Burp Proxy configuration.
    
6. **Activate Proxy Configuration:** Click on the FoxyProxy icon at the top-right of the Firefox browser and select the `Burp` configuration. This will redirect your browser traffic through `127.0.0.1:8080`. Note that Burp Suite must be running for your browser to make requests when this configuration is activated.
    
    ![](https://tryhackme-images.s3.amazonaws.com/user-uploads/5d9e176315f8850e719252ed/room-content/20f5e9db304d164b57c7f7d89fabc63a.png)
    
7. **Enable Proxy Intercept in Burp Suite:** Switch to Burp Suite and ensure that Intercept is turned on in the **Proxy** tab.
    
    ![](https://tryhackme-images.s3.amazonaws.com/user-uploads/645b19f5d5848d004ab9c9e2/room-content/9e0f6f47486737deff0e16c4e066120f.png)  
    
8. **Test the Proxy:** Open Firefox and try accessing a website, such as the homepage for `http://10.10.58.26/`. Your browser will hang, and the proxy will populate with the HTTP request. Congratulations, you have successfully intercepted your first request!
    

**Remember the following:**

- When the proxy configuration is active, and the intercept is switched on in Burp Suite, your browser will hang whenever you make a request.
- Be cautious not to leave the intercept switched on unintentionally, as it can prevent your browser from making any requests.
- Right-clicking on a request in Burp Suite allows you to perform various actions, such as forwarding, dropping, sending to other tools, or selecting options from the right-click menu.

Take note of these details as you begin using the Burp Suite Proxy.