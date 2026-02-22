                                          🧪 Lab 02 – Forensic Imaging with ProDiscover & FTK Imager



📘 Overview
This lab focused on the forensic acquisition of digital evidence from USB drives using ProDiscover and FTK Imager. The goal was to create exact, verifiable copies of source media while maintaining data integrity. The exercise emphasized proper imaging workflows, cryptographic hashing, and understanding the differences between EVE and E01 forensic image formats.

🎯 Objectives
1. Acquire forensic images from USB drives using industry‑standard tools.
2. Preserve evidence integrity using MD5 and SHA‑1 hashing.
3. Compare imaging formats (.EVE vs .E01) and their forensic relevance.
4. Document examiner details, case numbers, and metadata.
5. Understand how forensic tools verify image authenticity.

🛠️ Tools Used
1. ProDiscover Basic — Creates EVE images; manual hashing required.
2. FTK Imager — Creates E01 images with automatic hash generation.
3. MD5 & SHA‑1 — Cryptographic hashing algorithms for integrity checks.
4. Windows OS — Environment for imaging operations.

🔍 Key Activities
1. Selected USB drives as source media and configured destination paths.
2. Captured forensic images using ProDiscover and recorded MD5/SHA‑1 hashes.
3. Created E01 images using FTK Imager with built‑in verification hashes.
4. Added examiner information, case numbers, and evidence descriptions.
5. Compared computed, stored, and report hashes to confirm image integrity.
6. Reviewed the structure and purpose of EVE and E01 formats.
7. Documented bad sectors encountered during imaging.

🧾 Findings
1. ProDiscover generated .EVE images and required manual hashing.
2. FTK Imager generated .E01 images and automatically produced:
3. Computed hash
4. Stored verification hash
5. Report hash
6. All matched, confirming the integrity of the acquired images.
7. E01 images included examiner metadata and case details, making them more suitable for professional investigations.
8. MD5 and SHA‑1 values were successfully generated for each image.
9. Bad sectors were identified, highlighting the importance of documenting media condition.

📚 What I Learned
1. How forensic imaging tools preserve evidence without modifying original media.
2. Differences between EVE (ProDiscover) and E01 (EnCase/FTK) formats.
3. How hashing ensures authenticity and integrity of digital evidence.
4. How FTK Imager structures metadata and verification hashes for legal use.
5. The importance of examiner notes, case numbers, and chain‑of‑custody documentation.


