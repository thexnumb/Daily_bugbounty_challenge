1. **Review + Learning**
	1. what we do yesterday?
	2. for now we have nothing to learn!
	3. Reading write-up
		1. https://medium.com/@ahmed.elshaepe/all-about-javascript-analysis-for-bug-bounty-hunting-3e0f941c9676
2. **Hunting**
	1. re-organize the notes and write-down all the notes that should be written.
	2. start the recon
		1. subdomain discovery
			1. use the `thexrecon`
		2. certificate search
			1. `crt.sh`
			2. `shodan.io` - not work for today 
		3. run the `httpx_full` that get the all resolved subdomains
		4. run this command on all subdomains of the target
			1. `cat all_subs.txt | dnsx -resp-only -silent | sort -u | cut-cdn -silent | get_ip_asn | sort -u | get_asn_details >> all_subs_asn_details.txt`.
		5. doing the dorking
		6. struggling with the `js` file and trying to find maybe sensitive data