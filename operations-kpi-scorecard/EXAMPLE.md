# Operations KPI scorecard: an invented example

*Illustrative example with invented data.* The business, the people, the customers, the products, the figures and every date below are invented. The business is an invented 70-person wholesale distributor of catering and cleaning supplies, with one warehouse and its own delivery vans. Its operations manager runs the scorecard; the warehouse manager, the purchasing lead, the customer service lead and the transport manager each own measures. Customers appear as letters.

The operations review for October was held on the morning of Monday 2 November 2026, and the action it agreed was added to the action list. The operations manager then ran the scorecard. The inputs come first, in full, so the template can be run on them. The scorecard the workflow template returned follows.

## The inputs

### 1. Settings (typed by the operations manager)

```
Month being scored: October 2026
Today: Monday 2 November 2026
Operations review: Monday 2 November 2026, held this morning
Operations manager role: Operations manager
```

### 2. Measure sheet (set by the operations manager)

```
code,measure,definition,formula,source_file,period_column,unit,better,target,red,owner,type
M1,On-time dispatch,Share of orders dispatched on or before the date promised to the customer,orders_on_time / orders_dispatched × 100,wms_monthly.csv,month,%,higher,97.0,93.0,Warehouse manager,lagging
M2,Pick errors,Order lines picked wrongly for every 1000 lines picked,pick_errors / lines_picked × 1000,wms_monthly.csv,month,per 1000 lines,lower,2.0,4.0,Warehouse manager,lagging
M3,Picking productivity,Order lines picked for every hour worked in the warehouse,lines_picked / labour_hours,wms_monthly.csv,month,lines per hour,higher,55.0,48.0,Warehouse manager,lagging
M4,Core range out of stock,Core-range items with no stock available at month end,count of rows where core_range = Y and available = 0,low_stock_2026-10-31.csv,snapshot_date,items,lower,5,12,Purchasing lead,leading
M5,Customer complaints,Complaints logged for every 1000 orders dispatched,count of rows in complaints.csv / orders_dispatched in wms_monthly.csv × 1000,complaints.csv; wms_monthly.csv,logged_date; month,per 1000 orders,lower,2.0,4.0,Customer service lead,lagging
M6,Failed first deliveries,Share of delivery drops not completed at the first attempt,failed_first_attempt / drops × 100,transport_monthly.csv,month,%,lower,2.0,4.0,Transport manager,lagging
M7,Vehicle checks done,Share of daily vehicle checks due that were completed,vehicle_checks_done / vehicle_checks_due × 100,transport_monthly.csv,month,%,higher,100.0,95.0,Transport team,leading
```

### 3. Warehouse summary export: wms_monthly.csv

```
month,orders_dispatched,orders_on_time,lines_picked,pick_errors,labour_hours
2026-09,3985,3790,59420,154,1024
2026-10,4120,3828,61850,262,1105
```

### 4. Low-stock export: low_stock_2026-10-31.csv

```
sku,description,core_range,available,reorder_point,snapshot_date
C-1042,Nitrile gloves medium box of 100,Y,0,40,2026-10-31
C-1043,Nitrile gloves large box of 100,Y,0,40,2026-10-31
C-2210,Catering foil 450 mm roll,Y,0,25,2026-10-31
C-2211,Catering foil 300 mm roll,Y,0,25,2026-10-31
C-3105,Takeaway container 650 ml pack of 250,Y,0,30,2026-10-31
C-3320,Paper napkins white pack of 500,Y,6,30,2026-10-31
C-4018,Blue roll 2-ply case of 6,Y,0,20,2026-10-31
C-4502,Food-safe sanitiser 5 l,Y,0,15,2026-10-31
S-7781,Bamboo skewers 250 mm pack of 1000,N,0,10,2026-10-31
S-7914,Cake boxes 10 inch pack of 50,N,0,8,2026-10-31
```

### 5. Complaints log export: complaints.csv

```
ref,logged_date,customer,category,order_ref
CP-0412,2026-09-30,Customer K,Wrong item,SO-58811
CP-0413,2026-10-02,Customer B,Late delivery,SO-59020
CP-0414,2026-10-06,Customer F,Wrong item,SO-59133
CP-0415,2026-10-08,Customer A,Damaged,SO-59207
CP-0416,2026-10-12,Customer F,Wrong item,SO-59388
CP-0417,2026-10-14,Customer M,Short delivery,SO-59460
CP-0418,2026-10-19,Customer C,Late delivery,SO-59611
CP-0419,2026-10-21,Customer H,Wrong item,SO-59702
CP-0420,2026-10-27,Customer D,Wrong item,SO-59899
CP-0421,2026-10-30,Customer B,Late delivery,SO-59980
CP-0422,2026-11-01,Customer G,Damaged,SO-60014
```

### 6. Transport summary export: transport_monthly.csv

```
month,drops,failed_first_attempt,vehicle_checks_due,vehicle_checks_done
2026-09,3302,73,520,518
2026-10,3460,62,546,541
```

### 7. Scorecard history: scorecard_history.csv

```
code,month,value,status
M1,2026-08,97.4,GREEN
M1,2026-09,95.1,AMBER
M2,2026-08,2.1,AMBER
M2,2026-09,2.6,AMBER
M3,2026-08,57.2,GREEN
M3,2026-09,58.0,GREEN
M4,2026-08,6,AMBER
M4,2026-09,4,GREEN
M5,2026-08,1.7,GREEN
M5,2026-09,1.5,GREEN
M6,2026-08,2.3,AMBER
M6,2026-09,2.2,AMBER
M7,2026-08,98.4,AMBER
M7,2026-09,99.6,AMBER
```

### 8. Action list: actions.csv

```
ref,code,action,owner,due,status,agreed_on
A1,M1,Add a second packer on the dispatch bench on Mondays and Tuesdays,Warehouse manager,2026-10-19,Done,2026-10-05
A2,M2,Fit scan-to-confirm on the twenty fastest-moving pick faces,Warehouse manager,2026-10-30,In progress,2026-10-05
A3,M7,Shift lead signs off the Saturday vehicle checks,Transport manager,2026-10-31,Open,2026-10-05
A4,M2,Pair each agency picker with an experienced picker for their first two weeks on the floor,Warehouse manager,2026-11-13,Open,2026-11-02
```

### 9. Owners' notes

```
M1 (warehouse manager): Two experienced pickers left at the end of
  September and the four agency pickers who replaced them started on
  5 October. Most late orders were in the weeks of 5 and 12 October.
M2 (warehouse manager): Mis-picks rose with the new agency pickers.
  Scan-to-confirm is fitted on twelve of the twenty pick faces; the last
  eight are waiting for brackets.
M4 (purchasing lead): Two suppliers short-shipped gloves and catering
  foil. Both deliveries are due on 6 November.
M6 (transport manager): Fewer failed drops on the rural routes this
  month; nothing changed in how we run them.
M7 (transport manager): Five checks were missed, all on Saturday shifts,
  when no supervisor is on site.
```

## The output

**OPERATIONS KPI SCORECARD: October 2026**

**For:** Operations manager, for the operations review on Monday 2 November 2026. Prepared Monday 2 November 2026 from the measure sheet (7 measures), wms_monthly.csv, low_stock_2026-10-31.csv, complaints.csv and transport_monthly.csv, the scorecard history (August and September 2026), the action list (4 actions) and owners' notes for M1, M2, M4, M6 and M7.

**Overall:** 2 red, 3 amber, 2 green, 0 not rated.

**Scorecard**

- **M1 On-time dispatch:** 92.9%. **RED.** Target 97.0%; red at 93.0%; higher is better. Trend: August 97.4% · September 95.1% · October 92.9%, worse on last month, worse two months running. Owner: Warehouse manager.
- **M2 Pick errors:** 4.2 per 1000 lines. **RED.** Target 2.0; red at 4.0; lower is better. Trend: August 2.1 · September 2.6 · October 4.2, worse on last month, worse two months running. Owner: Warehouse manager.
- **M3 Picking productivity:** 56.0 lines per hour. **GREEN.** Target 55.0; red at 48.0; higher is better. Trend: August 57.2 · September 58.0 · October 56.0, worse on last month. Owner: Warehouse manager.
- **M4 Core range out of stock:** 7 items. **AMBER.** Target 5; red at 12; lower is better. Trend: August 6 · September 4 · October 7, worse on last month. Owner: Purchasing lead.
- **M5 Customer complaints:** 2.2 per 1000 orders. **AMBER.** Target 2.0; red at 4.0; lower is better. Trend: August 1.7 · September 1.5 · October 2.2, worse on last month. Owner: Customer service lead.
- **M6 Failed first deliveries:** 1.8%. **GREEN.** Target 2.0%; red at 4.0%; lower is better. Trend: August 2.3% · September 2.2% · October 1.8%, better on last month, better two months running. Owner: Transport manager.
- **M7 Vehicle checks done:** 99.1%. **AMBER.** Target 100.0%; red at 95.0%; higher is better. Trend: August 98.4% · September 99.6% · October 99.1%, worse on last month. Owner: Transport team. **FLAG:** the owner is a team, not one person. See question 2.

**How each value was worked out**

- **M1:** 3,828 / 4,120 × 100 = 92.9%. From wms_monthly.csv, the row for 2026-10.
- **M2:** 262 / 61,850 × 1,000 = 4.2. From wms_monthly.csv, the row for 2026-10.
- **M3:** 61,850 / 1,105 = 56.0. From wms_monthly.csv, the row for 2026-10.
- **M4:** count of rows with core_range Y and available 0 = 7. From low_stock_2026-10-31.csv, 10 rows dated 31 October 2026. Rows left out: 3, because C-3320 has 6 available and S-7781 and S-7914 are not core range.
- **M5:** 9 / 4,120 × 1,000 = 2.2. From complaints.csv, 9 rows logged in October 2026, and wms_monthly.csv, the row for 2026-10. Rows left out: 2, because CP-0412 was logged on 30 September and CP-0422 on 1 November.
- **M6:** 62 / 3,460 × 100 = 1.8%. From transport_monthly.csv, the row for 2026-10.
- **M7:** 541 / 546 × 100 = 99.1%. From transport_monthly.csv, the row for 2026-10.

**What moved**

- **M1 On-time dispatch,** AMBER to RED (95.1% to 92.9%): "Two experienced pickers left at the end of September and the four agency pickers who replaced them started on 5 October. Most late orders were in the weeks of 5 and 12 October."
- **M2 Pick errors,** AMBER to RED (2.6 to 4.2): "Mis-picks rose with the new agency pickers. Scan-to-confirm is fitted on twelve of the twenty pick faces; the last eight are waiting for brackets."
- **M4 Core range out of stock,** GREEN to AMBER (4 to 7): "Two suppliers short-shipped gloves and catering foil. Both deliveries are due on 6 November."
- **M5 Customer complaints,** GREEN to AMBER (1.5 to 2.2): reason not given by the owner.
- **M6 Failed first deliveries,** AMBER to GREEN (2.2% to 1.8%): "Fewer failed drops on the rural routes this month; nothing changed in how we run them."

**Reds and the actions agreed**

- **M1 On-time dispatch,** 92.9%: No open action agreed. See question 1.
- **M2 Pick errors,** 4.2 per 1000 lines: A2 Fit scan-to-confirm on the twenty fastest-moving pick faces, owner Warehouse manager, due 30 October 2026, In progress.
- **M2 Pick errors,** 4.2 per 1000 lines: A4 Pair each agency picker with an experienced picker for their first two weeks on the floor, owner Warehouse manager, due 13 November 2026, Open.

**Ambers**

- **M4 Core range out of stock,** 7 items: 2 items from target, 5 items before red. "Two suppliers short-shipped gloves and catering foil. Both deliveries are due on 6 November."
- **M5 Customer complaints,** 2.2 per 1000 orders: 0.2 from target, 1.8 before red. No note.
- **M7 Vehicle checks done,** 99.1%: 0.9 points from target, 4.1 points before red. "Five checks were missed, all on Saturday shifts, when no supervisor is on site."

**Last month's actions**

- **A1** (M1) Add a second packer on the dispatch bench on Mondays and Tuesdays, owner Warehouse manager, due 19 October 2026: Done.
- **A2** (M2) Fit scan-to-confirm on the twenty fastest-moving pick faces, owner Warehouse manager, due 30 October 2026: In progress, OVERDUE.
- **A3** (M7) Shift lead signs off the Saturday vehicle checks, owner Transport manager, due 31 October 2026: Open, OVERDUE.

**Measure sheet checks**

Measures: 7 of at most ten. Leading: M4, M7. M7: the owner is given as "Transport team", a team rather than one person.

**Questions for the operations manager**

1. M1 On-time dispatch is red at 92.9% and worse two months running. Its only action, A1, is done, and no open action is agreed for it. What action is agreed for M1, who owns it, and by when?
2. M7 Vehicle checks done names "Transport team" as its owner. Which one person owns M7?
3. A2 (M2), scan-to-confirm on the twenty fastest-moving pick faces, was due on 30 October 2026 and is in progress; the warehouse manager's note says twelve of the twenty are fitted. What is its new due date?
4. A3 (M7), the shift lead's sign-off of the Saturday vehicle checks, was due on 31 October 2026 and is open. What is its new due date?

Draft for the operations manager's review. Every value traces to the exports named above. Nothing has been sent, posted or changed, and the assistant has set no measure, target, owner or action.
