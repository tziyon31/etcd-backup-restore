ETCD Backup & Restore — Troubleshoot
<p align="center"> <img alt="Mission Badge" src="https://img.shields.io/badge/Mission-Control%20Plane-blue" /> <img alt="Kubernetes" src="https://img.shields.io/badge/Kubernetes-Cluster-lightgrey" /> <img alt="etcd v3" src="https://img.shields.io/badge/etcd-v3-important" /> <img alt="Disaster Recovery" src="https://img.shields.io/badge/Disaster%20Recovery-Ready-success" /> </p>

<h2>My first mission: The controlplane node in our cluster is planned for a regular maintenance reboot tonight. While we do not anticipate anything to go wrong, we are required to take the necessary backups. Take a snapshot of the ETCD database using the built-in snapshot functionality. Store the backup file at location /opt/snapshot-pre-boot.db</h2>

<img width="1264" height="677" alt="image" src="https://github.com/user-attachments/assets/09988248-60f3-4f40-a732-d85e575ca9b8" />
<img width="855" height="344" alt="image" src="https://github.com/user-attachments/assets/82c4df69-91df-41a5-9829-0dd1f28893cb" />
Using grep to find paths and Taking Snapshot
<img width="1051" height="526" alt="image" src="https://github.com/user-attachments/assets/5eb8aea7-3a63-42d1-8eab-f8647472c53b" />
My next task: Wake up! We have a conference call! After the reboot the master nodes came back online, but none of our applications are accessible. Check the status of the applications on the cluster. What's wrong?
<img width="604" height="66" alt="image" src="https://github.com/user-attachments/assets/661a5742-d816-4d9f-bfeb-0b7fa482b91e" />
Nothing is present!
Luckily we took a backup. Restore the original state of the cluster using the backup file.
Lets first verify the snapshot:
<img width="1224" height="768" alt="image" src="https://github.com/user-attachments/assets/446317dc-c0bf-470b-92b2-147216aa47a6" />
<img width="744" height="116" alt="image" src="https://github.com/user-attachments/assets/847e608b-9133-4313-a5fd-e47aa8b6a779" />
Stopping API Server
<img width="455" height="25" alt="image" src="https://github.com/user-attachments/assets/cda9f269-9f66-4292-ad51-83f90a34c66a" />
Restoring to New Directory
<img width="1053" height="264" alt="image" src="https://github.com/user-attachments/assets/4719a39c-6269-4eda-ae4b-fcc5aa0fc1f8" />
Adjusting ETCD.yaml
<img width="328" height="43" alt="image" src="https://github.com/user-attachments/assets/c433c873-2b7d-465d-8c02-44ef4b8c36be" />
Mission Accomplished!
<img width="772" height="398" alt="image" src="https://github.com/user-attachments/assets/24fb4f77-8a38-4cd6-ace8-b76a419b56bd" />




