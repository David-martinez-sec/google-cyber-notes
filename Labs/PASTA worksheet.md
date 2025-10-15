## PASTA worksheet

---

| Stages | Sneaker company |
| :---- | :---- |
| **I. Define business and security objectives** | The app will connect buyers and sellers with transactions occurring within the app. Business objectives and regulatory compliance will require user data protection per GDPR and PCI DSS  |
| **II. Define the technical scope** | *Public key infrastructure (PKI)* The objective of the app is to provide a method for transactions to occur between two parties. Prioritizing PKI ensures that those transactions are securely encrypted. Risk from key compromise lead to data breach, data tampering, and regulatory non-compliance.  |
| **III. Decompose application** | [Sample data flow diagram](https://docs.google.com/presentation/d/1ol7y79popTFfNHM-90ES-H-i1Lpd0YNvPShxBlXozjg/template/preview?resourcekey=0-DZAkf7Vzh2PXsP-j3oXV-g) |
| **IV. Threat analysis** | An internal threat to application data is from a social engineering attack vector targeting employee credentials. An external threat exists from PKI exploits such as a man-in-the-middle attack.  |
| **V. Vulnerability analysis** | The  application uses third-party api’s to add functionality, but also increases attack surface.  Lack of input validation on user input can lead to injection attacks.  |
| **VI. Attack modeling** | [Sample attack tree diagram](https://docs.google.com/presentation/d/1FmWLyHgmq9XQoVuMxOym2PHO8IuedCkan4moYnI-EJ0/template/preview?usp=sharing&resourcekey=0-zYPY7AhPJdcClXamlAfOag) |
| **VII. Risk analysis and impact** | Technical controls include Multi-Factor-Authentication  and Role Based access control. Operational controls include awareness training for common social engineering attacks, and  regular updates to patch vulnerable third-party apps |

---

