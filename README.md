# QRP CMC Choke (PCB)

A PCB for a lightweight QRP common-mode choke — rated for **up to 10 W (SSB & CW)** or **5 W on FT8**.

![PCB v1.1](/images/PCB_v11.png)

---

### Overview
This common-mode choke (CMC) is built around an **Amidon FT82-43** core with a smaller **FT50-43** core nested inside it. The nested arrangement yields a compact, low-loss choke with improved high-frequency behaviour compared with a single core of the same outer size — an excellent choice for QRP use where minimal dissipation and a small form factor matter.

---

### Recommended cores
- **Outer core:** Amidon FT82-43 (or Fair-Rite equivalent 5943000601)  
- **Inner core:** Amidon / Fair-Rite FT50-43 (5943001101) placed inside the FT82-43  
- **Alternative (high bands only):** Würth 74270118 — performs well on higher frequencies but **not recommended below ~6 MHz**.

---

### Practical guidance
- For 40–10 m common-mode suppression, many builders start with **~8–10 symmetrical turns**, which are usually sufficient for typical QRP antenna setups.  
- More turns increase common-mode impedance at lower frequencies, but also raise inter-winding capacitance — measure and adjust for your target bands.  
- Aim for **at least 20 dB of common-mode attenuation** across the target band where practical.  
- Target an **SWR as close to 1:1 as possible** after installing the choke; SWR below **1.5:1** is generally acceptable for most QRP uses.

**Wire & mechanical tips**
- Use enamelled copper wire sized appropriately for your power and mechanical needs — commonly 0.4–0.8 mm enamelled wire works well for QRP.  
- Keep pigtails and external leads short to avoid added series inductance.  
- Secure the nested cores mechanically with non-conductive tape or heat-shrink to prevent rotation or movement.

---

### How to test the CMC choke
Recommended guide (detailed):  
- Measuring common-mode choke performance — Lance Conry.  
  https://lance.conryclan.com/home/measuring-common-mode-choke-performance/

Quick checklist:
1. **Calibrate** your VNA (or impedance meter) for the measurement band.  
2. **Measure insertion loss / S21** in common-mode configuration to estimate attenuation.  
3. **Measure impedance / Z** vs frequency to verify target common-mode impedance.  
4. **Verify SWR** of your antenna/system with the choke installed to confirm no adverse effects.  
5. Iterate turns and retest until you hit the desired tradeoff between attenuation and bandwidth.

---

### Build results from v1.0

![PCB v1.0](/images/PCB_v1_0.png)

| Band | CMC attenuation (dB) | Insertion loss (dB) | VSWR |
|---|---:|---:|---:|
| 80 m  | -29.63 dB | -0.09 dB | 1.008 |
| 40 m  | -32.78 dB | -0.21 dB | 1.014 |
| 30 m  | -33.96 dB | -0.29 dB | 1.019 |
| 20 m  | -34.39 dB | -0.32 dB | 1.026 |
| 17 m  | -34.16 dB | -0.24 dB | 1.037 |
| 15 m  | -33.45 dB | -0.11 dB | 1.047 |
| 12 m  | -32.24 dB | +0.11 dB | 1.059 |
| 10 m  | -30.62 dB | +0.37 dB | 1.073 |

## Build / Manufacture

You can order this PCB from JLCPCB or any other service using the provided Gerber archive.

**Download Gerber**  
`./gerbers/qrp-cmc-pcb-v1.1-gerber.zip` 

### Recommended settings
Use the following manufacturing parameters when placing the order:

- **Board thickness:** `1.6 mm`  
- **Layers:** `2 (two-layer)`  
- **Material:** `FR-4`  
- **Copper weight:** `1 oz (35 µm)`  
- **Solder mask:** Chose your preferred

### 73s de YT3MW
