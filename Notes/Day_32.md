1. **Review + Learning**
	1. What is **Scope Discovery?**
		1. First main step on the Recon is Scope Discovery
		2. What is **Scope?**
			1. Scope specifies which subdomains, domains, products and overall which assets allows to attack.
		3. Once we have verify all the assets, then main focus is trying to find all domains, subdomains, IPs and trying to find which company is the organization hosting of these assets
		4. Steps
			1. WHOIS and Reverse WHOIS
				1. Companies or Individuals while register domain name, they should supply identification information like name, address, phone number and email address. so anyone can query these information with `whois` command which search for the owner's information of a domain.
				2. These information can be unavailable when use the `domain privacy` service. a third-party service replace user's information via a forwarding service
				3. We can do a reverse WHOIS search by searching a database for Organization name, phone number, email address to find other belongs of that user
					1. Use the [ViewDNS.info](https://viewdns.info/reversewhois)
2. 2. **Hunting**
	1. doing the `whois` and `reverse whois`