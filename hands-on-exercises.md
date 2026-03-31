# Hands-On Exercises: WEPPcloud and PATH

## After the Flames 2026 — Monday, April 6

**Goal:** Gain familiarity with the WEPPcloud interface and outputs through goal-directed exploration.

Use the pre-loaded WEPPcloud project to answer the questions below. Work individually or in small groups. Presenters are available to help if you get stuck.

**Note:** These exercises use uncalibrated watershed runs and are for demonstrative purposes only.

---

## Exercise 1: Exploring Soil Properties Across the Watershed

**Project:** https://wepp.cloud/weppcloud/runs/neurogenic-pendant/disturbed9002_wbt/

**Question:** Does the lower end of the watershed have more or less rock content than the upper portion?

**Steps:**

1. From the project run page, navigate to the **WEPP Run Results** section
2. Open the **GL-Dashboard** and wait for it to load
3. Go to the **Soils** section and select **"Rock content (%)"** to display the choropleth map
4. Hover over hillslopes in the upper and lower portions of the watershed to compare their rock content values

**What you should find:** The lower portion of the watershed has notably lower rock content than the upper portion.

---

## Exercise 2: Identifying Burn Severity Distribution

**Project:** https://wepp.cloud/weppcloud/runs/aversive-forestry/disturbed9002_wbt/

This is the Gate Creek watershed using the Holiday Farm Soil Burn Severity (SBS) map.

**Question:** What portion of the watershed burned at high severity?

**Steps:**

1. Open the project run page
2. Look at the **Soil Burn Severity** control — it provides a summary of burn severity class by percentage. Note that this table describes the SBS *map* coverage, not the watershed landuse breakdown
3. Instead, scroll to the **Landuse** control summary, which lists landuse classes by percentage of the watershed

**What you should find:** High Severity Fire accounts for 12.8% of the watershed. In WEPPcloud, the "Low Severity Fire," "Moderate Severity Fire," and "High Severity Fire" landuse classes refer to *forest*. Shrub and grass landcover types will include the cover type in their name (e.g., "Shrub High Severity Fire").

---

## Exercise 3: Return Periods and Storm Event Analysis

**Project:** https://wepp.cloud/weppcloud/runs/weatherproof-pickpocket/disturbed9002_wbt/

This is the Blackwood watershed at Lake Tahoe.

**Question:** What is the 25-year return period for Peak Discharge, and what are the characteristics of that storm event?

**Steps:**

1. On the project run page, scroll to the **WEPP Run Results** section and click on the **Return Periods Report** summary
2. Find the **Peak Discharge** table and locate the **25-year return period** — note the event date and discharge value
3. Now open the **Storm Event Analyzer**: click the **More** dropdown in the header at the top of the page, then select **PowerUser** to open the PowerUser Panel
4. In the PowerUser Panel, click **Storm Event Analyzer** in the far-right column to load the analyzer
5. Scroll down to the **Storm event hydrology characteristics** section and enter **93-06-03** in the Date field to load the event

**What you should find:** The 25-year return period Peak Discharge is approximately **630 ft³/s**, occurring on June 3, 1993. When you examine the storm event characteristics, notice that the prior day had snow coverage — this is a **rain-on-snow event**, which is an important driver of large peak discharges in this watershed.

---

## Exercise 4: Comparing Burned vs. Unburned Soil Loss with OMNI

**Project:** https://wepp.cloud/weppcloud/runs/aversive-forestry/disturbed9002_wbt/

This is the Gate Creek watershed (Holiday Farm fire) — the same project from Exercise 2.

**Question:** How does average annual Soil Loss compare between the burned and unburned scenarios?

### Part A: Burned Scenario Soil Loss

1. On the project run page, scroll to the **WEPP Run Results** section and click on the **Watershed Loss Summary**
2. Find and note the **Hillslope Soil Loss** in tonne/ha/yr

### Part B: Unburned (Undisturbed) Scenario Soil Loss

1. Return to the run page and scroll to the **Omni Scenarios** summary section
2. Click on **"undisturbed"** to open the undisturbed scenario run — the run ID should show as `aversive-forestry;;omni;;undisturbed`
3. Open the **Watershed Loss Summary** and note the **Hillslope Soil Loss** in tonne/ha/yr
4. Compare the two values

### Part C: Difference Map

1. Close the `aversive-forestry;;omni;;undisturbed` run and return to the main `aversive-forestry` project
2. Open the **GL-Dashboard**
3. Change the **selected scenario** to **undisturbed** and click **Compare to Base Scenario**
4. Expand the **WEPP** section and select the **Soil Loss** radio button to view a difference map
5. Now visually compare this difference map to the **Dominant landuse** map for the burned scenario

**What you should find:** There is a clear correspondence between hillslopes with increased soil loss and those classified as high burn severity. The difference map highlights where fire has the greatest impact on erosion relative to undisturbed conditions.

---

## Exercise 5: Finding the Highest Soil Loss Hillslope

**Project:** https://wepp.cloud/weppcloud/runs/aversive-forestry/disturbed9002_wbt/

Continuing with the Gate Creek watershed.

**Question:** Which hillslope generated the most soil loss, and where is it in the watershed?

**Steps:**

1. Open the **Watershed Loss Summary** and scroll down to the **Hillslope Summary Table**
2. Click on the **Soil Loss** column header to sort the table by Soil Loss — it will sort in ascending order
3. Click the header a **second time** to sort in descending order
4. Note the **Topaz ID** for the top hillslope (1693)
5. Return to the run page and scroll up to the **map control**
6. In the **"Center or ID search"** field, enter **1693** and click the **Find Topaz ID** button
7. Watch for the corresponding hillslope to flash on the map for a few seconds

**What you should find:** Hillslope 1693 generated the most soil loss. When you locate it on the map, notice that it is a notably steep hillslope — slope is a key driver of erosion.

