# Task 1: Check File and Directory Details

To ensure proper permissions and security.

## Steps:

1. Use the following command to list all files, including hidden ones, along with their permissions, ownership, and group information:
   ```bash
   ls -la /home/researcher2/projects
<img width="1002" alt="Screenshot 2024-09-05 at 16 41 21" src="https://github.com/user-attachments/assets/33e2819b-108b-4da1-9324-ec6c67ca7407">

# Task 2: Change File Permissions

you must determine whether any files have incorrect permissions and then change the permissions as needed. This action will remove unauthorized access and strengthen security on the system.

## Objective:
Ensure that **none of the files** in the `/home/researcher2/projects` directory allow **other users** to have write permissions.

### Steps:

1. **Check Permissions:**
   - Use the following command to check whether any files in the `projects` directory have write permissions for the "other" user type:
     ```bash
     find /home/researcher2/projects -type f -perm /o=w
     ```
   - This command will list any files that have write permissions for "others" (`o=w`).

2. **Change Permissions (if necessary):**
   - Change the permissions of the file identified in the previous step so that the owner type of other doesn’t have write permissions.
     ```bash
     chmod o-w project_k.txt
     ```
   - In the chmod command, u sets the permissions for the user who owns the file, g sets the permissions for the group that owns the file, and o sets the permissions for others.

3. **Verify Permissions:**
   - After changing the permissions, verify that no files in the directory have write access for other users by running the same check again:
     ```bash
     find /home/researcher2/projects -type f -perm /o=w
     ```

By completing this task, you will ensure that no unauthorized users have write access to any files, enhancing the system's security.

