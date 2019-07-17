# Charles-Proxy-Andriod-SSL-Debugging-Tutorial
Android 7+ API debugging tips using charles proxy

- Written and maintained by Shirshak


1. Root Your Phone with Magisk
2. Install Root file browser because we need to move charles certificate
3. From charles proxy save charles-ssl-proxying-certificate.pem file
4. Run these command on terminal
```
hash=$(openssl x509 -inform PEM -subject_hash_old -in charles-ssl-proxying-certificate.pem | head -1)
mv charles-ssl-proxying-certificate.pem "$hash.0"
```
5. There will be new file with extension .0 please move that file using root file manager to /system/etc/security/cacerts/
6. Setup proxy in mobile and happy debugging.

If there is problem raise issue and I can write this in detail


## Certificate Pinning
Most app like facebook, banking app use certificate pinning. We can use Frida framework. I will write this part once I am free. If you are facing problem in certificate pinning please open issue.
