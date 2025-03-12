# Configure Account Password Policies

In this video, we will use **Local Security Policy** under **Windows Administrative Tools** to configure Password Restrictions.



https://github.com/user-attachments/assets/f3b7bf8d-5ef1-4087-ad49-5e812a734d6a



## Account Security Requirements:
1. **Password History**: Users cannot reuse any of the last **4** passwords.
2. **Password Expiration**: Passwords must be changed every **30** days.
3. **Minimum Password Age**: New passwords cannot be changed for at least **2** days.
4. **Password Length**: Passwords must be at least **10** characters long.
5. **Password Complexity**: Must be **Enabled**
6. **Account Lockout**: After **4** incorrect attempts lockout for **40** minutes, Unlock Automatically after **60** minutes.

### Walkthrough

1. Click on **Start** navigate to **Windows Administrative Tools** and select on **Local Security Policy**.
2. Expand **Account Policies** from the left pane
3. Click on **Password Policy** in order to make our changes.
4. Click on **Account Lockout Policy** in order to make our changes.
