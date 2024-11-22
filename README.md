# Lets-Defend-Incident-Response-7

**SOC138 - Detected Suspicious Xls File**

**Summary:**

During this incident response the alert was triggered from a malicious XLS file. Response started with checking the network logs, seeing that the user Sophia had made request to a malicious IP. This inturn compramised the system. The logs were checked and she was the only endpoint affected. The endpoint was contained from the rest of the network.

**Incident Response:**

After Creating the case, taking ownership, and starting then playbook.

I note all data given so far.

<img width="713" alt="Screenshot 2024-11-22 111748" src="https://github.com/user-attachments/assets/8bc17943-e21c-432b-8c99-2640bbe8201f">

I check the logs inside the `Log Managment` tab for any traffic from the source IP: `172.16.17.56`

<img width="894" alt="Screenshot 2024-11-22 111637" src="https://github.com/user-attachments/assets/2c336244-05aa-446c-9e83-7e72571b35d9">

I can see 2 that have the correct date of Mar 13.

<img width="526" alt="Screenshot 2024-11-22 111959" src="https://github.com/user-attachments/assets/7ed941a6-870b-4251-84b7-635737535862">
<img width="516" alt="Screenshot 2024-11-22 112008" src="https://github.com/user-attachments/assets/83e5a157-e416-4e8e-a9f8-20807c5ff432">

I can see the destination IP now. I search that in the EDR to see if it is in network.

It is not.

Continuing with the playbook.

<img width="561" alt="Screenshot 2024-11-22 112231" src="https://github.com/user-attachments/assets/840a48f6-56e9-4a30-b3f3-27c6fb783d6d">

The threat indicator is Unkown or unexpected outgoing traffic.

![Screenshot 2024-11-22 112446](https://github.com/user-attachments/assets/543c55f5-836b-4c2d-90ad-fa4d879e67e7)

To check if the device is quartantined, since it is out of network. Looking back at data given device action was set to `allowed`. This proves it isnt quarantined.

![Screenshot 2024-11-22 112616](https://github.com/user-attachments/assets/921a97ac-ab57-4273-b617-704752ed83a4)

To see if it is malicous I will check the file hash in Virus Total and Cisco Talos.

![Screenshot 2024-11-22 113737](https://github.com/user-attachments/assets/cb486224-4113-43ee-9128-753331fb284e)

As we can see it has proven to be malicous.

![Screenshot 2024-11-22 114339](https://github.com/user-attachments/assets/771d2420-f89e-40d9-a57d-d268930d69ef)

As seen previously we can see the malicous IP has been accessed by a endpoint "Sofia".

![Screenshot 2024-11-22 114328](https://github.com/user-attachments/assets/5608b443-283d-4397-99fd-8f984cbb6ade)

Next step contain the Endpoint.

![Screenshot 2024-11-22 114456](https://github.com/user-attachments/assets/a15b4508-9891-452e-8503-926ea40f9787)

![Screenshot 2024-11-22 114958](https://github.com/user-attachments/assets/bb21b357-56af-4724-94d2-3e4719ba2d3d)

Add any artifcacts.

![Screenshot 2024-11-22 115151](https://github.com/user-attachments/assets/2d82be36-ea95-4b78-9b88-cc7c620c95c8)

![Screenshot 2024-11-22 115425](https://github.com/user-attachments/assets/24fbd89c-8f93-4856-94f6-00dd38355f11)
















