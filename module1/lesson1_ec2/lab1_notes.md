## COBOL Practice

- **Run used:** Run 1
- **Instance ID:** `i-0fd900238cdf69669`
- **Return code 0 — command and exact output:** `./cobol/bin/payment_post TXN-MN-0008 100001 1.00 USD INV-1008` — `STATUS=POSTED`, `REASON=APPROVED`; return code `0`.
- **Return code 4 — command and exact output:** `./cobol/bin/payment_post TXN-MN-0009 999999 10.00 USD INV-1009` — `STATUS=REJECTED`, `REASON=ACCOUNT NOT FOUND`; return code `4`.
- **Return code 8 — command and exact output:** `./cobol/bin/payment_post TXN-MN-0010 100001 999999.99 USD INV-1010` — `STATUS=REJECTED`, `REASON=INSUFFICIENT FUNDS`; return code `8`.
- **Return code 12 — command and exact output:** `./cobol/bin/payment_post` — `STATUS=REJECTED`, `REASON=MALFORMED REQUEST`, usage message displayed; return code `12`.
- **Alice's balance decoded using `cut -c`:** Account lookup showed Alice Johnson, account `100001`, balance `5000.00 USD`. The balance was not independently decoded from the fixed-width account file using `cut -c` yet.
- **Journal lines for my TXN IDs and whether the balance changed:** `payments.dat` contained transaction IDs `TXN-MN-0001`, `0002`, `0004`, `0005`, `0007`, `0008`, `0009`, and `0010`. The file records posted and rejected transactions. The balance change was not independently verified.

## Mistakes I made

- Initially used an incorrect file path when locating the runbook.
- Learned that command output, such as folder names printed by `ls`, should not be entered as commands.

## Commands I now know by heart

- `ls` — list files and directories.
- `cd` — change directories.
- `git clone` — clone a repository.
- `cut -c` — extract character ranges from fixed-width text.
- `echo $?` — display the previous command's exit code.
- `whoami && TZ='America/Denver' date && ec2-metadata -i && uptime -s` — record the user, local time, EC2 instance ID, and boot time.