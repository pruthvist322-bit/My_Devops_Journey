# Day 26 – Domain Purchase, AWS Route 53 & HTTPS Setup

Today, I learned how to purchase a domain, connect it with AWS, and secure it using an SSL/TLS certificate.

## What I Learned

* Purchased a custom domain (Example: **raniapp.in**).
* Created a **Hosted Zone** in AWS Route 53 using the purchased domain name.
* After creating the hosted zone, AWS generated four **Name Servers (NS)**.
* Logged into the domain registrar where the domain was purchased.
* Opened the **DNS/Name Server** settings and replaced the existing name servers with the four name servers provided by Route 53.
* Once the DNS changes propagated, the hosted zone became active.
* Created an **A Record (Alias)** in Route 53 and mapped it to the AWS Application Load Balancer.
* Since the application was initially accessible only over HTTP, I learned how to enable HTTPS.
* Requested an SSL/TLS certificate using AWS Certificate Manager (ACM) by providing the fully qualified domain name.
* Validated the certificate by creating the required DNS validation record in Route 53.
* After the certificate was issued, updated the Load Balancer listener from **HTTP (Port 80)** to **HTTPS (Port 443)** and attached the SSL certificate.
* Finally, accessed the application using the custom domain and verified that the website was secured with HTTPS.

## Key Takeaways

* Understood how DNS works with AWS Route 53.
* Learned the purpose of Name Servers and Hosted Zones.
* Gained hands-on experience configuring DNS records.
* Learned how SSL/TLS certificates are issued and validated.
* Successfully hosted a secure website using a custom domain and HTTPS.

**Day 26 Complete! 🚀**
