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

# Verifying File Ownership and Hidden Files

### Step 1: Verify File Ownership
The first step is to verify who owns the files in the `/home/researcher2/projects` directory.

#### Answer:
The `research_team` group owns the files in the `projects` directory.

---

### Step 2: Check for Hidden Files
Next, you need to check whether any hidden files exist within the `projects` directory. Hidden files typically start with a dot (`.`).

#### Command to Check for Hidden Files:
Use the following command to list all hidden files in the directory:

![Screenshot 2024-09-05 at 18 30 58](https://github.com/user-attachments/assets/d09f04fc-91fa-4ca0-b86a-31ca5507faa8)  

Answer: The .project_x.txt file is hidden.

# Task 3: Change File Permissions on a Hidden File

In this task, you will verify and, if necessary, modify the permissions on the hidden file `.project_x.txt`. This step is crucial for removing unauthorized access and strengthening the security of the system.

## File Information:
- **File**: `.project_x.txt` (Hidden file)
- **Requirement**: The file has been archived and should **not** be written to by anyone. The **user** and **group** should still retain read permissions.

## Steps to Complete:

1. **Check Current Permissions:**
   Use the following command to check the permissions of the hidden file `.project_x.txt`:
   ```bash
   ls -la /home/researcher2/projects/.project_x.txt


![Screenshot 2024-09-05 at 18 43 21](https://github.com/user-attachments/assets/01eab573-509e-4fde-a845-8fbf8ef4242c)

# Task 4: Change Directory Permissions

In this task, you will adjust the permissions of the `/home/researcher2/projects/drafts` directory to ensure proper access control. Specifically, only the `researcher2` user should have access to the `drafts` directory and its contents, meaning only `researcher2` should have execute privileges.

## Objective:
Ensure that the `researcher2` user has exclusive access to the `drafts` directory by modifying the permissions to remove the execute privileges for the group.

## Steps to Complete:

1. **Check Current Permissions:**
   Begin by checking the current permissions of the `drafts` directory while in the `projects` directory. Use the following command:
   ```bash
   ls -la /home/researcher2/projects/drafts

![Screenshot 2024-09-05 at 18 47 16](https://github.com/user-attachments/assets/f058688a-6d6b-439b-bf0a-f8c3ffa71674)
