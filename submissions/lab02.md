### ctf01

1. Vulnerability Discovery from Known URLs
recon04: `ad1d44d6-ab73-4640-8291-c5bf2343e2a5` (\admin)

2. Vulnerability detection from public files
recon01: `aeaee57f-2a82-41da-bc4c-d081c8cddfc8` (\..\..\..\key.txt 404 page)

3. Detecting vulnerabilities in Javascript files
ptlab_key_recon_26: `d6b75269-97a3-44de-be32-fff0dd55e7ef`

4. Web Server Vulnerability Detection
recon00: `af9c328a-02b4-439d-91c6-f46ab4a0835b `(\robots.txt)
`99d0738b-1e52-4a00-8885-b15894b2c79e` (\)
recon: `99685e30-7061-4ac0-83bf-4ccc0409faac` (/.well-known/security.txt)
recon01: `aeaee57f-2a82-41da-bc4c-d081c8cddfc8` (/whatever 404 page)

5. Vulnerability detection via IP address
recon06: ` 5cf83b5d-eb6c-4eee-af6c-945f9aed8dfd` (http://51.158.147.132/)

6. Vulnerability detection in repo3
`08be82ba-e5fd-4fae-b2c2-272a18d31f80`(https://github.com/hackycorp/repo3/tree/08be82ba-e5fd-4fae-b2c2-272a18d31f80)

7. Vulnerability detection in repo4
recon21: `a60b4aee-642a-483b-9262-ccfc2ed46f0d`

8. Vulnerability detection in repo9
`3ee505c2-8aa9-4d5e-810e-921778dce1e6`

.. continuing to solve the labs following the README description.

### ctf02

Solved the challenges following the description in README.

### ctf03

1. Who is the suspicious employee?
The suspicious employee is Evil Hacker, evil@company.com, IT.

2. What password was used in the system?
The first password used was `password123`, which was then replaced with the base64 encoded password `YWRtaW4xMjM=` or `admin123` decoded.
FLAG{weak_password}

3. Is there any hidden data in the image?
Yes, there is text appended to the end of the image: FLAG{cant_see_me}.

4. What is inside the backup file?
The backup file was encrypted using the password `admin123`, and contained one file: `secret.txt`.
FLAG{backup_leak}

5. Can you find any unusual activity in logs?
There is a Failed login attempt from the user `evil` from the IP 192.168.1.66
FLAG{suspicious_ip}

6. JWT log
FLAG{jwt_decoded}