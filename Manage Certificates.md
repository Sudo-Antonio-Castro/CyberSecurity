# Manage Certificates

In This video, we will manage certificates using the Certification Authority. We will approve, deny, revoke, and un-revoke certificates.



https://github.com/user-attachments/assets/170c112e-bb93-4a1f-8783-a0fa89665a8f



## Requirements
1. Look at **Pending Requests**.
3. Look at **Issued Certificates**.
4. Look at **Revoked Certificates**.

## Questions
1.**What is the purpose of manually approving smart card certificate requests in a corporate network?**

### Walkthrough

1. Within the **Hyper-V Manager** select the **CorpServer2** and Double-Click **CorpCA**.
2. Within the **Server Manager** select **Tools** and then **Certification Authority**.
3. Within the **certsrv** select **Pending Requests**.
4. Right click on user **mlopez** >>> **All Tasks** >>> **Issue**.
5. Right click on user **CorpSrv16** >>> **All Tasks** >>> **Deny** >>> **Yes**.
6. Select **Issued Certificates** >>> Right Click on user **bnguyen** >>> **All Tasks** >>> **Revoke Certificate**.
7. Under **Reason Code** Choose appropriate code, in this case it is **Key Compromise**.
8. Right Click on user **tsutton** >>> **All Tasks** >>> **Revoke Certificate**.
9. Under **Reason Code** Choose appropriate code, in this case it is **Change of Affiliation**.
10. Select **Revoked Certificates**, Right Click on **CorpDev2** >>> **All Tasks** >>> **Unrevoke Certificate**
