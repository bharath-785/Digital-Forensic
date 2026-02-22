                           🧪 Lab 03 – Forensic Image Analysis with ProDiscover & FTK Imager
📘 Overview

This lab focused on analyzing two previously acquired forensic images (USB‑Pro‑U and USB‑Pro‑F) using ProDiscover and FTK Imager. The goal was to examine the file systems, identify deleted or hidden artifacts, compute and verify hash values, and determine whether any suspicious or noteworthy files existed within the images. The analysis included reviewing NTFS metadata, unallocated space, deleted entries, and file slack.

🎯 Objectives

1. Load and analyze forensic images using ProDiscover and FTK Imager.
2. Compute and verify MD5 and SHA‑1 hash values for each image.
3. Identify file types, deleted files, and NTFS metadata structures.
4. Examine unallocated space and orphaned files.
5. Detect any suspicious or unusual files within the images.

🛠️ Tools Used

1. ProDiscover Basic — For viewing image contents, metadata, and deleted files.
2. FTK Imager — For browsing directory structures, unallocated space, and verifying hashes.
3. NTFS File System Structures — $MFT, $BadClus, $Recycle.Bin, $Extend, orphan files, and slack space.

🔍 Key Activities

🔹 Analysis in ProDiscover

1. Loaded the forensic images using File → Open Image.
2. Examined multiple views including Content View, Cluster View, Registry View, and Search Results.
3. Identified file types such as DOC, XLS, PNG, JPG, LOG, INI, DAT, and NTFS metadata files.
4. Located deleted files and examined their attributes.
5. Observed the presence of $BadClus:$Bad, a large NTFS metadata file used to track bad sectors.
6. Identified LairNetPutty.exe, a suspicious executable also seen in Lab 1.

🔹 Analysis in FTK Imager

1. Added images using File → Add Evidence Item → Image File.
2. Explored the Evidence Tree to review root, orphan, and unallocated directories.
3. Identified deleted entries such as I30 file slack, temporary files, and system metadata.
4. Examined $Recycle.Bin, System Volume Information, and NTFS system files.
5. Reviewed unallocated space blocks containing remnants of previous data.

🧾 Findings

🔹 Hash Values

USB‑Pro‑U
1. MD5: 79F0B5D05C44189598FA9611FE504AEC
2. SHA1: AFD20A96C5EEDD04AEFD649A9D381172CDD5DAF4
3. MD5 Checksum: ad08bb6f03af12b30b0cf7571439d8e6

USB‑Pro‑F
1. MD5: BBCAE44CD0834DE08271CFC5CE71BC5F
2. SHA1: 8F97BA5CC91CE7C58957456DFAD016F71D4F5603
3. MD5 Checksum: cf302355dbff780e924dc247cc63e6da

USB‑FTK‑U (E01 image)

1. MD5: 1af419c7daa1bb149efcd5cdcdb05339
2. SHA1: 72c7768243308f4a83caf1031fe91f70c2eba074

🔹 File System Observations

1. Both images contained a mix of documents, spreadsheets, images, logs, and system files.
2. Only a small number of files were marked as deleted.
3. $BadClus:$Bad was the largest file, indicating reserved bad sectors.
4. desktop.ini was found inside $RECYCLE.BIN, a normal Windows system file.
5. Multiple temporary (.tmp) files were present, some deleted.
6. Unallocated space contained numerous data fragments, typical of previously deleted content.
7. LairNetPutty.exe appeared again, consistent with earlier labs and potentially suspicious.

🔹 Suspicious or Notable Artifacts
1. LairNetPutty.exe — previously identified as malicious in Lab 1.
2. Deleted temporary files — may indicate prior activity or software installations.
3. Presence of file slack and unallocated remnants — useful for deeper forensic recovery.

📚 What I Learned

1. How to analyze forensic images using both ProDiscover and FTK Imager.
2. How NTFS metadata structures reveal deleted files, bad clusters, and system activity.
3. How to interpret unallocated space and file slack for hidden or deleted artifacts.
4. How to verify image integrity using MD5 and SHA‑1 hashing.
5. How to identify suspicious files within a forensic image and correlate findings across tools.
