# EBS
WORKING WITH EBS

## Aim

To create and configure an Amazon Elastic Block Store (EBS) volume, attach and mount it to an Amazon EC2 instance, create a snapshot backup, and restore the snapshot to a new EBS volume.

## Algorithm / Steps

1. Create a new Amazon EBS volume with a size of 1 GiB.
2. Select the same Availability Zone as the EC2 instance.
3. Attach the EBS volume to the EC2 instance using `/dev/sdb`.
4. Connect to the EC2 instance using AWS Systems Manager Session Manager.
5. Check the available storage using `df -h`.
6. Create an `ext3` file system on the EBS volume.
7. Create the `/mnt/data-store` directory.
8. Mount the EBS volume to `/mnt/data-store`.
9. Configure `/etc/fstab` for automatic mounting.
10. Verify that the EBS volume is successfully mounted.
11. Create `file.txt` inside the mounted EBS volume.
12. Verify the contents of the created file.
13. Create an EBS snapshot named `My Snapshot`.
14. Delete `file.txt` from the original EBS volume.
15. Create a new EBS volume from the snapshot.
16. Attach the restored volume to the EC2 instance using `/dev/sdc`.
17. Create the `/mnt/data-store2` directory.
18. Mount the restored volume to `/mnt/data-store2`.
19. Verify that `file.txt` has been successfully restored.

## Outputs
<img width="1920" height="1200" alt="Screenshot (233)" src="https://github.com/user-attachments/assets/35ef48f5-52a1-49b2-82f0-a4376975d831" />
<img width="1920" height="1200" alt="Screenshot (234)" src="https://github.com/user-attachments/assets/16a5ba07-6edb-475e-ab46-ffa2c6dd6594" />
<img width="1920" height="1200" alt="Screenshot (235)" src="https://github.com/user-attachments/assets/4257b57f-174d-41eb-8656-4ef7af32b608" />
<img width="1920" height="1200" alt="Screenshot (236)" src="https://github.com/user-attachments/assets/597518b4-5e66-428c-b801-582af48c6646" />
<img width="1920" height="1200" alt="Screenshot (237)" src="https://github.com/user-attachments/assets/4ab1c577-2235-4c9a-8144-1173f931760e" />
<img width="1918" height="930" alt="628586671-2f9931e1-fb42-4081-bb52-3c139de21c27" src="https://github.com/user-attachments/assets/e7702316-3fe1-4ced-99a5-c167a913167e" />
<img width="1920" height="1200" alt="Screenshot (238)" src="https://github.com/user-attachments/assets/b64bdc30-d080-4407-9da2-312211659e71" />
<img width="1920" height="1200" alt="Screenshot (239)" src="https://github.com/user-attachments/assets/57cbfee1-6773-47ed-9223-b94a3546574f" />

## Result
Thus, an Amazon EBS volume was successfully created and attached to an Amazon EC2 instance. The volume was formatted with an ext3 file system, mounted, and used for storing data. An EBS snapshot was successfully created as a backup, and a new EBS volume was restored from the snapshot. The previously deleted file.txt was successfully recovered, demonstrating the backup and restore functionality of Amazon EBS.
