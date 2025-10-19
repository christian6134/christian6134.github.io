"How Fast is Fast"

- Nmap provides various options to control the **scan speed and timing**

Running scans at normal speed may trigger an IDS or other security measures
`Use -T0 or -T 0 or -T paranoid` for the slowest timing

![[Pasted image 20250630155518.png]]


**Controlling the number of parallel service probes**
- `--min-parallelism <numprobes> and --max-parallelism<numprobes>`
- Probes decrease as packets drop more and increase as network runs flawlessly


**Controlling Rate at which Nmap sends packets**
- `--min-rate<number> and --max-rate <number>`
- Provided as number of packets per seconds
- Applies to the whole scan and not to a single host


