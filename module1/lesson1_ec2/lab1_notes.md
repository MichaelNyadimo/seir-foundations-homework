# Lesson 1 — EC2 Lab Notes

## Run 1 — Instance ID: `i-0dd3ee21e4d686b`

I launched the first EC2 instance and connected to it to begin the lab. I practiced navigating the project files and running application commands. I also experimented with the COBOL exercises and learned how different return codes represent different outcomes.

**Exact output:**
```text
Fri OCT 30 23:05:19 MDT 2026
Instance ID: i-0dd3ee21e4d686b
```

## Run 2 — Instance ID: `i-018ffab3c18989f29`

I created another EC2 instance to repeat the lab process. I practiced connecting to the instance using SSH and checking that the application environment was available. I learned how repeating the process helps confirm that the setup works across multiple EC2 instances.

**Exact output:** 

Instance ID: `i-018ffab3c18989f29` 
2026-10-31 02:31:41

## Run 3 — Instance ID: `i-06f400daefd0e5e0d`

I completed another EC2 deployment and practiced the connection and application startup process. I verified that the application was accessible after connecting to the instance. I also became more comfortable with the deployment process.

**Exact output:**
Instance ID: `i-06f400daefd0e5e0d`
2026-10-31 04:12:14

## Run 4 — Instance ID: `i-0d36009dd1448dd0`

I completed the fourth EC2 run and captured screenshots of the process. I continued practicing the commands used to inspect the instance and run the application. I learned the importance of collecting evidence while the instance was running so the deployment could be documented.

**Exact output:**
Instance ID: `i-0d36009dd1448dd0`
2026-10-31 16:45:26

## Run 5 — Instance ID: `i-0cb9ac50a592ffd2`

I launched and connected to the fifth EC2 instance. I repeated the application checks and saved screenshots of the results. This run reinforced the importance of verifying that the application is working rather than relying only on the instance launch status.

**Exact output:** 
Instance ID: `i-0cb9ac50a592ffd2`
2026-10-31 17:23:12

## Run 6 — Instance ID: `i-0e6975e519b4d31f8`

I completed the sixth EC2 run and continued practicing the deployment workflow. I checked the application and captured the required screenshots. I gained more confidence connecting to EC2 instances and documenting the results.

**Exact output:** 
Instance ID: `i-0e6975e519b4d31f8`
2026-10-31 17:43:02

## Run 7 — Instance ID: `i-044eea7d2bf947f8c`

I completed the seventh EC2 run and captured the final set of screenshots. I repeated the connection and application checks to confirm that the lab workflow was working. This final run gave me additional practice deploying, accessing, and documenting EC2 instances.

**Exact output:** 
Instance ID: `i-044eea7d2bf947f8c`
2026-11-01 20:00:29
## COBOL Practice

- **Run used:** Run 7
- **Instance ID recorded for COBOL practice:** `i-044eea7d2bf947f8c`
- **Return code 0:**
  - Command: `./cobol/bin/payment_post TXN-MN-0008 100001 1.00 USD INV-1008`
  - Output: `STATUS=POSTED`, `REASON=APPROVED`
- **Return code 4:**
  - Command: `./cobol/bin/payment_post TXN-MN-0009 999999 10.00 USD INV-1009`
  - Output: `STATUS=REJECTED`, `REASON=ACCOUNT NOT FOUND`
- **Return code 8:**
  - Command: `./cobol/bin/payment_post TXN-MN-0010 100001 999999.99 USD INV-1010`
  - Output: `STATUS=REJECTED`, `REASON=INSUFFICIENT FUNDS`
- **Return code 12:**
  - Command: `./cobol/bin/payment_post`
  - Output: `STATUS=REJECTED`, `REASON=MALFORMED REQUEST`; a usage message was displayed.
- **Alice's account:** Account `100001`, Alice Johnson, with a balance of `5000.00 USD`.
- **Payment journal:** The journal contained transaction IDs `TXN-MN-0001`, `0002`, `0004`, `0005`, `0007`, `0008`, `0009`, and `0010`.

## Mistakes I made

- I initially used an incorrect file path when locating the runbook.
- I entered directory names printed by `ls` as if they were commands.
- I had to repeat some setup steps, including checking that port 8000 was available.

## Commands I now know by heart

- `ls` — list files and directories.
- `cd` — change directories.
- `git clone` — clone a Git repository.
- `cut -c` — extract character ranges from fixed-width text.
- `echo $?` — display the previous command's exit code.
