# Hands-On Exercises: WEPPcloud and PATH

## After the Flames 2026 — Monday, April 6

**Goal:** Gain familiarity with the WEPPcloud interface and outputs through goal-directed exploration.

Use the pre-loaded WEPPcloud project to answer the questions below. Work individually or in small groups. Presenters are available to help if you get stuck.

**Note:** These exercises use uncalibrated watershed runs and are for demonstrative purposes only.

---

## Exercise 1: Exploring Soil Properties Across the Watershed

**Project:** [aversive-forestry/disturbed9002_wbt](https://wepp.cloud/weppcloud/runs/aversive-forestry/disturbed9002_wbt/)

**Question:** Does the lower end of the watershed have more or less rock content than the upper portion?

**Steps:**

1. From the project run page, navigate to the **Run Results** section by clicking on **WEPP** in the **Preflight and navigation** panel and then look for the **Run Results** section after **WEPP**
2. Open the **GL-Dashboard** and wait for it to load
3. Go to the **Soils** section in the layer panel on the left and select **"Rock content (%)"** to display the choropleth map. You may need to scroll down to find the **Soils**
4. Hover over hillslopes in the upper and lower portions of the watershed to compare their rock content values

**What you should find:** The lower portion of the watershed has notably lower rock content than the upper portion.

**For fun:** Explore other soil properties!

---

## Exercise 2: Identifying Burn Severity Distribution

**Project:** [aversive-forestry/disturbed9002_wbt](https://wepp.cloud/weppcloud/runs/aversive-forestry/disturbed9002_wbt/)

This is the Gate Creek watershed using the Holiday Farm Soil Burn Severity (SBS) map.

**Question:** What portion of the watershed burned at high severity?

**Steps:**

1. Open the project run page
2. Look at the **Soil Burn Severity** control — it provides a summary of burn severity class by percentage. Note that this table describes the SBS *map* coverage, not the watershed landuse breakdown
3. Instead, scroll to the **Landuse** control summary, which lists landuse classes by percentage of the watershed

**What you should find:** High Severity Fire accounts for 12.8% of the watershed. In WEPPcloud, the "Low Severity Fire," "Moderate Severity Fire," and "High Severity Fire" landuse classes refer to *forest*. Shrub and grass landcover types will include the cover type in their name (e.g., "Shrub High Severity Fire").

---

## Exercise 3: Return Periods and Storm Event Analysis

**Project:** [weatherproof-pickpocket/disturbed9002_wbt](https://wepp.cloud/weppcloud/runs/weatherproof-pickpocket/disturbed9002_wbt/)

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

**Project:** [aversive-forestry/disturbed9002_wbt](https://wepp.cloud/weppcloud/runs/aversive-forestry/disturbed9002_wbt/)

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

**Project:** [aversive-forestry/disturbed9002_wbt](https://wepp.cloud/weppcloud/runs/aversive-forestry/disturbed9002_wbt/)

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

---

## Exercise 6: Finding Hillslope Data 

**Report:** [PATH Cost-Effective Report](https://jackson-nakae.github.io/PATH-cost-effective/)

**Exercise:** Identify two hillslopes on the map with different treatments and record their slope, burn severity, acreage, and final sediment yield.

**Steps:**

1. Select Section 2 in the Table of Contents.
2. Scroll to the 'Interactive Map of Selected Hillslopes' in section 2.1.
3. Use you mouse to hover over a hillslope on the map to see information for each hillslope.
4. Note that different shades of green represent the different mulch treatments (0.5 tons/acre, 1 ton/acre, and 2 tons/acre) as indicated in the legend in the lower right-hand corner of the map.
5. Now identify two hillslopes with different mulch treatments (as shown through different shades of green).
6. Hover over each and take note of the following information: slope, burn severity, acreage, and final sediment yield.


**What you should find:** The map allows you to access the information for each hillslope by hovering over the desired hillslope. Hillslopes with various green shades are those that PATH recomends recieve treatment. Mulch treatments of larger quantities (darker green shades) are often recommended on hillslopes with a large sediment yield (sdyd) post-fire, steep slopes, and/or those that have been burned more severely. 

---

## Exercise 7: Hillslopes that exceed the Sediment Yield Threshold

**Report:** [PATH Cost-Effective Report](https://jackson-nakae.github.io/PATH-cost-effective/)

**Question:** What is the minimum Hillslope Sediment Yield Threshold value that results in no hillslopes exceeding the sdyd threshold?

**Steps:**

1. Select Section 3 from the Table of Contents.
2. Scroll to the 'Interactive Hillslope Selection Map' in Section 3.1.
3. Using the Hillslope Sediment Yield Threshold slider, reduce the threshold to zero. You should see many hillslopes outlined in red. Hillslopes are outlined in red when thier sediment yield does not meet the Sediment Yield Threshold despite recieving the most effective treatment.
4. Now increase this threshold until there are no hillslopes outlined in red and STOP.
5. Record the Sediment Yield Threshold value indicated on the slider.

**What you should find:** Once the Hillslope Sediment Yield Threshold reaches a value of **9 tons/acre** there are no longer any hillslopes outlined in red. This means that after the recommended treatments all hillslopes considered for treatment will meet this threshold.

## You May Notice ##

After exploring the features of this interactive map in section 3.1 you may notice that even under the strictest threshold values not all hillslopes in the catchment are receiving treatment. This is because in this example PATH used Omni Contrasts Cumulative Objective Parameter mode with a 90% Cumulative Objective Threshold Fraction on Soil Loss. Therefore, the only hillslopes considered for treatment are those that contribute to soil loss up to this threshold.



