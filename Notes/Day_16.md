- review
- hunting
	- setup the get ASN from IP
	- The functions that is helpful for recon (ASN discovery)
		```bash
				get_ip_asn () {
		    while read -r ip; do
		        curl -s "https://api.bgpview.io/ip/$ip" | jq -r '.data.prefixes[].asn.asn' | sort -u
		    done
		}
		get_asn_details () {
		        while read -r asn
		        do
		                curl -s "https://api.bgpview.io/asn/$asn" | jq -r '.data | {asn, name, description_full, email_contacts}'
		        done
		}
		get_shodan_hostnames () {
	        curl -s https://internetdb.shodan.io/$1 | jq -r ".hostnames[]"
		}
		```
	- full flow of doing ASN discovery
		- `echo subdomains.txt | sort -u | dnsx -resp-only | sort -u | cut-cdn -silent | get_ip_asn | sort -u | get_asn_details`
	- full flow for doing Domain discovery
		- `echo CIDR | mapcidr -silent | while read ip; do get_shodan_hostnames $ip 2> /dev/null; done | sort -u | tee all_domains.txt`


- **I/O Streams**
    - `stdin`
        - used to read input from the user
        - file descriptor = 0
            - it is a number that belong to processes
        - so we get our input from here
    - `stdout`
        - used to display output to the terminal
        - file descriptor = 1
        - in fact it is the output
    - `stderr`
        - used to display error messages to the terminal
        - for show the errors
        - file descriptor = 2