# Linux Server Administration & Nginx Reverse Proxy

## Internship
RabTech Academy - Cloud Computing & DevOps

## Project Overview
This project demonstrates Nginx reverse proxy configuration and basic Linux server administration using Ubuntu on WSL2.

## Features
- Nginx reverse proxy to a Python test application
- Gzip compression
- Request rate limiting
- Cache-Control response headers
- Self-signed SSL/TLS certificate for local HTTPS testing
- UFW firewall rules for ports 22, 80, and 443
- Linux configuration documentation

## Project Structure
- app/index.html - Test application page
- nginx/reverse-proxy.conf - Nginx configuration
- docs/linux-configuration.md - Project documentation
- screenshots/ - Project screenshots

## Testing
Validate Nginx:
sudo nginx -t

Test HTTP:
curl http://localhost

Test local HTTPS:
curl -k https://localhost

## Environment Notes
This project was tested in Ubuntu on WSL2. The SSL certificate is self-signed and intended for local testing only.

SSH key-based authentication and production hardening must be verified before deploying to a public server.
