# README: WISP SB_2024 Lubac D² Analysis

What this notebook does:
- Loads the WISP SB_2024 reflectance dataset (csv, 1 nm grid, 350–900 nm)
- Applies the Lubac D² method to classify each spectrum as P. globosa-like (1) or not (0)
- Summarizes results, diagnostics, and provides a ready-to-report management conclusion

How to use:
1. Download the real *`WISP_wp2cs3_sodra_bergundasjon_all_months_2024_0930.csv`* dataset from sharepoint 
2. Replace the existing dummy file at the location `data\raw\SB_2024\WISP_wp2cs3_sodra_bergundasjon_all_months_2024_930_QA_data.csv`
3. Rename the downloaded file to make sure that the file name ends with `<>_QA_data.csv` to maintain compatibility with the code
4. Set/update its path (in cell 2 of [notebooks\wp2_cs3\01_lake_sb_wisp_tests.ipynb](01_lake_sb_wisp_tests.ipynb))
5. Run all cells in order
6. Review the summary and diagnostics at the end for key findings and action points

About the data:
- Source: WISP sensor, Södra Bergundasjon, 2024 campaign
- Format: 
    - Each row = one spectrum
    - Data columns = `datetime, id, name, wl_350_nm ... wl_900_nm`.
- No pre-filtering or manual editing required

Output:
- Table of Lubac D² results (P_LUB)
- Diagnostics on classifier logic
- Summary of results and action points *(recommendations)*

PS: 
Data location on [Aquatime SharePoint](https://brockmannconsult.sharepoint.com/sites/AQUATIME/Shared%20Documents/Forms/AllItems.aspx):
- Original raw xlsx file: [WISP Spectra SWE Södra Bergundasjön 2024.xlsx](https://brockmannconsult.sharepoint.com/:x:/r/sites/AQUATIME/Shared%20Documents/WP2%20Representative%20Dataset/Case_Study_3/S%C3%B6dra%20Bergundasj%C3%B6n/Hyperspectral%20data/WISP%20Spectra%20SWE%20S%C3%B6dra%20Bergundasj%C3%B6n%202024.xlsx?d=wf0c373246c4c4a0a8cb82d31a88f56b0&csf=1&web=1&e=0wMNx5)
- Processed WISP Spectra SWE Södra Bergundasjön: [WISP_wp2cs3_sodra_bergundasjon_all_months_2024_0930.csv](https://brockmannconsult.sharepoint.com/sites/AQUATIME/Shared%20Documents/WP2%20Representative%20Dataset/Case_Study_3/S%C3%B6dra%20Bergundasj%C3%B6n/Hyperspectral%20data/processed_hyperspectral_data/WISP_wp2cs3_sodra_bergundasjon_all_months_2024_0930.csv?d=w4c7ef3cc0c624ed1b0745ac8bcc0ff90), **this dataset has been used here**