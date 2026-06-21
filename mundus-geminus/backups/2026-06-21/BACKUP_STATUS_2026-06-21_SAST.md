# Mundus Geminus Backup Status — 2026-06-21 SAST

Backup ID: `MG-KADE-BACKUP-2026-06-21-SAST-001`

## GitHub

Status: SUCCESS

Repository: `Naerys28/Kades-backup-hub-`

Snapshot path:
`mundus-geminus/backups/2026-06-21/PROJECT_BACKUP_2026-06-21_SAST.md`

Snapshot commit:
`eaaa00488352e59b3a61d7903c98aaf1a04f6485`

## Google Drive

Status: SUCCESS

Folder:
`Mundus Geminus - Private Emergency Archive - 2026-06-18`

Folder ID:
`1Lt6q972OV834bg5LstOeOKgxtKVtYCNH`

Document:
`Mundus Geminus Project Backup 2026-06-21 SAST`

Document ID:
`1oEEV0ukbmy6neYF1CBVLvQh-4G6aLnJlXPiuxJCW-yE`

Document URL:
https://docs.google.com/document/d/1oEEV0ukbmy6neYF1CBVLvQh-4G6aLnJlXPiuxJCW-yE/edit?usp=drivesdk

## Neon

Status: PARTIAL SUCCESS

Project:
`Mundus Geminus`

Project ID:
`rough-term-18563940`

Fresh backup branch created:
`backup-project-snapshot-2026-06-21-sast`

Fresh backup branch ID:
`br-summer-lake-abl6yx51`

Parent branch:
`br-quiet-cake-abf99v4j` / `production`

Neon branch URL:
https://console.neon.tech/app/projects/rough-term-18563940/branches/br-summer-lake-abl6yx51

SQL row write status: BLOCKED

Reason returned by Neon direct SQL connection:
`NeonDbError: This connection is trying to access this endpoint from a blocked network.`

Meaning:
- Neon API branch creation worked.
- Direct SQL write into `kade_backup.project_snapshots` did not work from this environment because the database endpoint is blocked/vaulted.
- The full readable snapshot exists in GitHub and Drive.
- Neon has a fresh checkpoint branch, but not the full snapshot row.

## Integrity Note

This status file is written so nobody mistakes the Neon part for a full row-level content backup. GitHub and Drive are complete readable mirrors. Neon is branch-level only until the network/vault restriction is lifted or an allowed SQL path is provided.
