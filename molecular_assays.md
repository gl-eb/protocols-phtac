---
title: Molecular Assays
subtitle: "Version 1.7"
version: "1.7"
---

## PCR

Protocol adapted Macarena Toll-Riera and Promega

1. Harvest bacterial cells to run PCR on
   - Liquid culture:
      1. Transfer 20 µL of bacterial culture into a centrifuge tube containing 80 µL of sterile MilliQ
      2. Centrifuge at maximum speed for 3 minutes
      3. Discard supernatant and resuspend pellets in 50 µL sterile MilliQ
   - Colonies: Barely touch the colony with a pipette tip, place in 50 µL of sterile MilliQ and pipette up and down a few times
2. Incubate at 95°C for 10 minutes in heating block
3. Centrifuge at maximum speed for 5 minutes
4. Store at 4°C
5. Perform PCR using the GoTaq G2 Green Master Mix (includes most reagents needed for PCR and a gel)
   1. Prepare a master mix for n + 1 reactions of 25 µL each
      - 12.5 µL GoTaq G2 Green Master Mix
      - 1.25 µL forward primer (10 µM)
      - 1.25 µL reverse primer (10 µM)
      - 8.75 µL nuclease-free water
   2. Add 23.75 µL of master mix to PCR tubes and add 1.25 µL DNA template to each
   3. Gently vortex and then briefly centrifuge reactions
   4. Start PCR program (cycle through steps 2-4 30 times; this will take just under 2 hours)
      1. Initial Denaturation for 2 min at 95°C
      2. Denaturation for 30 s at 95°C
      3. Annealing for 30 s at T~m~ -- 5°C
         - Use lower T~m~ of each primer pair to calculate annealing temperature
         - Higher temperatures make annealing more specific
      4. Elongation for 1 min/kb at 72°C
      5. Final Elongation for 5 min at 72°C
      6. Hold at 4°C
6. Run gel as a control that amplification worked
   1. Prepare 1% agarose gel
      1. Add 1g of agarose to 100 mL 1x TAE buffer inside erlenmeyer flask and microwave at standard settings for 1 minute
      2. Add 10 µL of SYBR Safe to the gel chamber
      3. Pour gel in small gel chamber with the comb appropriate for the number of samples. Use the comb to ensure SYBR Safe is properly mixed with the liquid
   2. Load 10 µL of a 1 kb ladder and PCR reaction directly into the gel (or 5 µL if using small wells)
   3. Run gel at 120V for 30 minutes and image it
   4. If PCR did not work, the DNA might have been too concentrated. Retry after dilluting the sample

## 16S rRNA Sequencing

1. Perform PCR according to [PCR]
   - Use one of the following primer pairs. Melting temperatures according to the [Promega calculator](https://ch.promega.com/resources/tools/biomath/tm-calculator/) specifically for use with GoTaq G2 Green Master Mix and 200 nM primers

     | Primer Pair         | Specificity                         | Source                                     |
     | --- | ----- | ---- |
     | 16s_fw + 16s_rv     | *Ph*TAC125 & *E. coli*              | Toll-Riera et al. 2022                     |
     | 16s_fw_2 + 16s_rv_2 | *Ph*TAC125                          | Gleb Ebert                                 |
     | F27 + R1525         | universal, two bands for *Ph*TAC125 | Lane et al. 1991, Stackebrandt et al. 1993 |

     | Primer Pair         | Annealing \[°C\] | Product \[bp\] | Elongation \[s\] |
     | ------------------- | ---------------: | -------------: | ---------------: |
     | 16s_fw + 16s_rv     |               60 |           1008 |               60 |
     | 16s_fw_2 + 16s_rv_2 |               60 |            946 |               60 |
     | F27 + R1525         |               57 |           1528 |               90 |

     | Name     | Sequence               | T~m~ \[°C\] |
     | -------- | ---------------------- | ----------: |
     | 16s_fw   | GATCATGGCTCAGATTGAACGC |          65 |
     | 16s_rv   | AGGCACCAAACCATCTCTGG   |          65 |
     | 16s_fw_2 | CCACACTGGGACTGAGACAC   |          65 |
     | 16s_rv_2 | GCACTCTGTATGCGCCATTG   |          65 |
     | F27      | AGAGTTTGATCCTGGCTCAG   |          62 |
     | R1525    | AAGGAGGTGATCCAGCCGCA   |          69 |

2. PCR cleanup according to one of the following options:
   - Use the Promega Wizard SV Gel and PCR Cleanup System or the Qiagen QIAquick PCR Purification Kit according to the respective manufacturer protocols. Elute with 30 µL of nuclease free water
   - According to protocol adapted from Macarena Toll-Riera
     1. Mix PCR cleanup reaction
        - 17 µL PCR product
        - 0.3 µL Exonuclease I
        - 0.3 µL Antarctic Phosphatase
        - 2.4 µL sterile MilliQ (to fill up volume)
        - Prepare a master mix for multiple reactions (n + 1) and add 3 µL to each tube
     2. Incubate samples in thermocycler or waterbath
        1. 15 minutes at 37°C
        2. 15 minutes at 80-85°C
        3. Hold at 4°C
3. Measure DNA concentration and purity using the GDC's NanoDrop. 260/280 (protein purity) and 260/230 (salt purity) should both be between 1.8 and 2.0. The latter often tends to be as small as 1.2, even after using a PCR cleanup kit
4. Calculate the necessary dilution factor to reach a final DNA concentration of 1.5 ng/µL per 100 bp of PCR product after adding primers. Taking this into account, the target DNA concentration before addition of primers should be:
   $$ \text{target concentration} = \frac{\text{product length}\ bp}{100\ bp}*1.5 \frac{ng}{\mu L}*\frac{15\ \mu L}{12\ \mu L} $$
   E.g. for a 1.5 kb product the target concentration should 28.125 ng/µL
5. Prepare samples for sequencing by adding to each shipping tube
   - 12 µL purified PCR reaction at the appropriate DNA concentration
   - 3 µL 20 µM primer (just one, either forward or reverse)
6. Add Microsynth label to tube and register samples online. Print out order summary and package it in a clear plastic bag together with the samples
7. Bring samples to Microsynth pickup point at the main entrance of the LFV building
