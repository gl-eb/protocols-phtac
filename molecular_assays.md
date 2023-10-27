---
subtitle: "Version 1.5"
title: "Molecular Assays"
---


## PCR

Protocol adapted from Penn iGEM 2013, Spencer Glantz, Kathleen Sproufffske, Macarena Toll-Riera, Promega

1. Harvest bacterial cells to run PCR on
   - PCR from liquid culture:
      1. Transfer 20 uL of bacterial culture into a centrifuge tube containing 80 uL of sterile MilliQ
      2. Centrifuge at maximum speed for 3 minutes
      3. Discard supernatant and resuspend pellets in 50 uL sterile MilliQ
   - PCR from colonies: Barely touch the colony with a pipette tip, place in 50 uL of sterile MilliQ and pipette up and down a few times
2. Incubate at 95°C for 10 minutes in heating block
3. Centrifuge at maximum speed for 5 minutes
4. Store at 4°C
5. Perform PCR using the GoTaq G2 Green Master Mix (it's very easy and already includes everything needed for PCR and the gel)
   1. Thaw master mix at room temperature
   2. For 25 uL reaction volume combine
      - 12.5 uL GoTaq G2 Green Master Mix
      - 1.25 uL forward primer (10 uM)
      - 1.25 uL reverse primer (10 uM)
      - 1.25 uL DNA
      - 8.75 uL nuclease-free water
   3. Centrifuge reactions for 5 s
   4. Start PCR program (cycle through steps 2-4 30 times; this will take just under 2 hours)
      1. Initial Denaturation for 2 min at 95°C
      2. Denaturation for 30 s at 95°C
      3. Annealing for 30 s at T~m~ - 5°C (when in doubt, use 50 - 55°C; lower temperatures make annealing more conservative in general)
      4. Elongation for 1 min/kb at 72°C
      5. Final Elongation for 5 min at 72°C
      6. Hold at 4°C
6. Run gel as a control that amplification worked
   1. Prepare 1% agarose gel (in K17)
      1. Add 1g of agarose to 100 mL 1x TAE buffer inside erlenmeyer flask and microwave at standard settings for 1 minute
      2. Add 10 uL of SYBR Safe to the gel chamber
      3. Pour gel in small gel chamber with the comb appropriate for the number of samples. Use the comb to ensure SYBR Safe is properly mixed with the liquid
   2. Load 10 uL of a 1 kb ladder and PCR reaction directly into the gel (or 5 uL if using small wells)
   3. Run gel at 120V for 30 minutes and image it
   4. If PCR did not work, the DNA might have been too concentrated. Retry after dilluting the sample

## 16S rRNA Sequencing

1. Perform PCR according to [PCR]
   - Use one of the following primer pairs. Melting temperatures according to the [Promega calculator](https://ch.promega.com/resources/tools/biomath/tm-calculator/)

     | Name     | Sequence               | T~m~ | Specificity                         | Source                   |
     | -------- | ----------------------------------- | ---- | ----------------------- | ----------------------- |
     | 16s_fw   | GATCATGGCTCAGATTGAACGC | 66°C | *Ph*TAC125 & *E. coli*              | Macarena Toll-Riera      |
     | 16s_rv   | AGGCACCAAACCATCTCTGG   | 66°C | *Ph*TAC125 & *E. coli*              | Macarena Toll-Riera      |
     | 16s_fw_2 | CCACACTGGGACTGAGACAC   | 66°C | *Ph*TAC125                          | Gleb Ebert               |
     | 16s_rv_2 | GCACTCTGTATGCGCCATTG   | 66°C | *Ph*TAC125                          | Gleb Ebert               |
     | F27      | AGAGTTTGATCCTGGCTCAG   | 63°C | universal, two bands for *Ph*TAC125 | Lane et al. 1991         |
     | R1525    | AAGGAGGTGATCCAGCCGCA   | 70°C | universal, two bands for *Ph*TAC125 | Stackebrandt et al. 1993 |

   - Elongation time: ~1.5 kb -> 2 min
2. PCR cleanup according to one of the following options:
   - Use the Promega Wizard SV Gel and PCR Cleanup System or the Qiagen QIAquick PCR Purification Kit according to the respective manufacturer protocols. Elute with 30 uL of nuclease free water. This ensures at least two sequencing runs if necessary
   - According to protocol adapted from Sinisa Bratulic, Kathleen Sprouffske Macarena Toll-Riera
     1. Mix PCR cleanup reaction
        - 17 uL PCR product
        - 0.3 uL Exonuclease I
        - 0.3 uL Antarctic Phosphatase
        - 2.4 uL sterile MilliQ (to fill up volume)
        - Prepare a master mix for multiple reactions (n + 1) and add 3 uL to each tube
     2. Incubate samples in thermocycler or waterbath
        1. 15 minutes at 37°C
        2. 15 minutes at 80-85°C
        3. Hold at 4°C
3. Measure DNA concentration and purity using the GDC's NanoDrop. 260/280 (protein purity) and 260/230 (salt purity) should both be between 1.8 and 2.0. The latter often tends to be as small as 1.2, even after using a PCR cleanup kit
4. Calculate the necessary dilution factor to reach a final DNA concentration of 1.5 ng/uL per 100 bp of PCR product after adding primers. Taking this into account, the target DNA concentration before addition of primers should be: $$ \text{target concentration} = \frac{\text{product length}}{100}*1.5*\frac{15}{12} $$ E.g. for a 1.5 kb product the target concentration should 28.125 ng/uL
5. Prepare samples for sequencing by adding to each shipping tube
   - 12 uL purified PCR reaction at the appropriate DNA concentration
   - 3 uL 20 uM primer (just one, either forward or reverse)
6. Add Microsynth label to tube and register samples online. Print out order summary and package it in a clear plastic bag together with the samples.
7. Bring samples to Microsynth pickup point at the main entrance of the LFV building
