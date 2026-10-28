# Linux Server Administration & Nginx Reverse Proxy

## 1. Project Overview
This project demonstrates Linux server administration and Nginx reverse proxy configuration for the RabTech Academy internship.

## 2. Environment
- Operating System: Ubuntu on WSL2
- Web Server: Nginx
- Reverse Proxy: Nginx
- Test Application: Python HTTP server
- Application Port: 3000
- HTTP Port: 80

## 3. Nginx Reverse Proxy
Nginx receives HTTP requests on port 80 and forwards them to the application running at 127.0.0.1:3000.

Features included:
- Reverse proxy forwarding
- Forwarded client and protocol headers
- Gzip compression
- Request rate limiting
- Cache-Control response headers
- Disabled Nginx server version tokens

## 4. Configuration and Testing
Configuration file: nginx/reverse-proxy.conf

Validation:
sudo nginx -t

Reload:
sudo systemctl reload nginx

Test:
curl http://localhost

Expected response:
<h1>RabTech Academy</h1><p>Nginx Reverse Proxy is working!</p>

## 5. SSH Security
SSH key-based authentication should be configured and tested before disabling password authentication. Password authentication must not be disabled until key-based login has been verified.

## 6. Firewall
Required firewall ports:
- SSH: TCP 22
- HTTP: TCP 80
- HTTPS: TCP 443

Firewall rules must be verified in the target environment. WSL2 networking may behave differently from a standalone Linux server.

## 7. SSL/TLS
HTTPS should use a valid TLS certificate for a deployed domain. A self-signed certificate can be used for local testing, but browsers will show a certificate warning.

## 8. Testing and Limitations
The reverse proxy was tested locally in Ubuntu on WSL2. This confirms the basic proxy configuration but does not prove public accessibility or production readiness.

SSH hardening, firewall configuration, and HTTPS must be completed and verified before claiming they are implemented.

## 9. Conclusion
The Nginx reverse proxy successfully forwards local HTTP requests to the test application. This project provides a foundation for further Linux server security and web-service deployment.
