# 纽约侧官方数据核验（第 1 轮）

核验日期：2026-10-10。说明：census.gov / data.census.gov / api.census.gov、bls.gov、mta.info、omny.info、data.cityofnewyork.us、a860-gpp.nyc.gov（DHS 日报）、comptroller.nyc.gov、osc.ny.gov 在本环境均返回 403 或无法连接，所以这些来源的数值只能取自其官方页面的搜索摘要，或取自引用它们的其他市/州官方文件；表中已逐条注明。

| 编号 | 指标 | 数值 | 年份 | 口径说明 | 来源（发布方+URL） | 可信度(官方/官媒转述/其他) | 备注 |
|---|---|---|---|---|---|---|---|
| NY-A1 | NYC（5 区）陆地面积 | 300.45 sq mi（约 778.2 km²） | 2020/2022 表 | 仅陆地面积，不含水域 | NYS Department of Health, Vital Statistics Table 2 — https://www.health.ny.gov/statistics/vital_statistics/2022/table02.htm | 官方（州政府） | 与 2022 参考值约 780 km² 一致；Census QuickFacts LND110220 页面无法打开 |
| NY-A2 | NYC 人口（2020 普查） | 8,804,190（普查值）；估算基数 8,805,594 | 2020 | 2020-04-01 十年普查 | U.S. Census Bureau QuickFacts — https://www.census.gov/quickfacts/fact/table/newyorkcitynewyork/HSG010223 | 官方（取自搜索摘要） | 8,804,190 这个普查值只在非官方转载中直接看到，QuickFacts 摘要显示的是估算基数 8,805,594 |
| NY-A3 | NYC 人口（最新估算） | 8,584,629（较 2020 −2.5%） | 2025-07-01 | Census Vintage 2025 人口估算 | U.S. Census Bureau QuickFacts — https://www.census.gov/quickfacts/fact/table/newyorkcitynewyork/HSG010223；NYC DCP 称约 8.58 million — https://www.nyc.gov/content/planning/pages/planning/population | 官方 | 两个来源一致 |
| NY-A4 | 纽约都会区人口 | 20,112 千人（约 2,011 万） | 2025-07-01 | New York-Newark-Jersey City, NY-NJ MSA（OMB 2023 定义，NASA 页面称共 23 个县；不含 CT 部分县） | U.S. Census Bureau 数据，由 FRED (Federal Reserve Bank of St. Louis) 转载，系列 NYTPOP — https://fred.stlouisfed.org/data/NYTPOP | 官方转述 | 2022 参考值约 2,300 万对应的是 CSA（New York-Newark, NY-NJ-CT-PA），不是 MSA，两者不能直接比；2025 年 CSA 官方值见“未找到”清单 |
| NY-B1 | NYC AMI（3 口之家，100% AMI） | $152,700 | 2026 | HUD 为 NYC 地区设定、HPD 发布的 AMI（另有 80% AMI 为 $122,160） | NYC HPD — https://www.nyc.gov/site/hpd/services-and-information/area-median-income.page | 官方 | 2021 年为 $107,400，涨幅较大，部分原因在于 HUD 的 AMI 是含高收入调整的地区口径 |
| NY-B2 | NYC 家庭收入中位数 | $81,228 | 2024 | ACS 2024 一年期，全部住户（租房户 $64,866，自有户 $121,443） | NYC Rent Guidelines Board, 2026 Income and Affordability Study（引用 ACS 2024）— https://rentguidelinesboard.cityofnewyork.us/wp-content/uploads/2026/04/2026-IA.pdf | 官方（市政机构转引 Census） | 名义值比 2023 年 +6.1%，实际值 +2.2% |
| NY-B3 | 纽约都会区家庭收入中位数 | NOT FOUND（官方） | — | — | 已查 Census ACSBR-025（2024 收入简报）页面/PDF，均被拦截 | — | 聚合站 Census Reporter 显示 MSA 为 $99,155（应为 2020-24 五年期），不合规，不采用 |
| NY-C1 | 租房户占比 | 67.7%（2,324,000 / 3,432,000 套有人居住单元） | 2023 | NYC HVS 2023，按有人居住单元计 | NYC HPD, 2023 NYCHVS Selected Initial Findings — https://www.nyc.gov/assets/hpd/downloads/pdfs/about/2023%20NYCHVS%20Selected%20Initial%20Findings.pdf | 官方 | 比例由报告中的户数算出；HVS 为三年一次，下一期是 2026 |
| NY-C2 | 租金中位数（gross rent） | $1,811/月（contract rent 为 $1,695） | 2024 | ACS 2024，全部租房户，gross rent 含另付的水电燃气 | NYC RGB 2026 I&A Presentation — https://rentguidelinesboard.cityofnewyork.us/wp-content/uploads/2026/04/2026-IA-Presentation.pdf | 官方 | 2019 参考值 $1,483。另 HVS 2023 contract rent 中位数为 $1,641（同上 HVS 报告），口径不同 |
| NY-C3 | 租金负担 >30% 的租房户占比 | 51.6%（ACS 2024）；HVS 2023 为 43%（25%+18%） | 2024 / 2023 | ACS：≥30% 收入用于 gross rent，全部租房户。HVS：>30%，不含公房和持租房券户 | ACS：NYC RGB 2026 I&A Presentation（同上）；HVS：NYC HPD 2023 NYCHVS（Table 18，同上） | 官方 | 两个口径不能混用 |
| NY-C4 | 租金负担 >50% 的租房户占比 | 28.8%（ACS 2024）；HVS 2023 为 25% | 2024 / 2023 | 同上；HVS 中收入 < $25,000 的租房户有 86% 属于严重负担 | 同 NY-C3 | 官方 | HVS 2023 租金收入比中位数为 29.5%；ACS 2024 gross rent 收入比中位数为 30.9% |
| NY-C5 | NYC 自有住房率 | 32.3%（HVS 2023，1,109,000 / 3,432,000）；ACS 2020-24 五年期 32.8% | 2023 / 2020-24 | 自有户 ÷ 有人居住单元 | NYC HPD 2023 NYCHVS（同上）；U.S. Census Bureau QuickFacts HSG445224 — https://www.census.gov/quickfacts/fact/table/newyorkcitynewyork/HSG445224 | 官方 | HVS 正文一处写成“2021 年 30%”，此处按 2023 年户数自行计算 |
| NY-C6 | 都会区自有住房率 | NOT FOUND | — | — | 已查 Census CPS/HVS “Homeownership Rates for the 75 Largest MSAs: 2015-2025”（https://www.census.gov/housing/hvs/data/rates.html），被拦截 | — | 页面截图可后续手动补 |
| NY-D1 | 地铁车站数 / 线路长度 | 472 座车站；客运线路近 250 英里（约 400 km）；轨道“650 英里以上” | 现行 | 472 为官方计数（换乘站按多座计）；250 mi 为线路长度；650+ mi 为轨道长度 | NYPD Transit Bureau — https://www.nyc.gov/site/nypd/bureaus/transit-housing/transit.page；NYC Mayor's Office of Climate & Environmental Justice — https://www.nyc.gov/content/climate/pages/public-transit；Governor Hochul 2026 讲话亦称 472 stations | 官方（市政转述 MTA） | MTA 官网“Subway and bus facts”页无法打开，最好再找 MTA 原页核对 |
| NY-D2 | 地铁年客流 | 近 13 亿人次（比 2024 年 +7%，相当于疫情前 85%） | 2025 | 地铁进站人次 | Office of Governor Hochul（MTA 联合公告）— https://www.governor.ny.gov/news/governor-hochul-highlights-record-breaking-year-performance-and-ridership-mta-2025 | 官方 | NYC Transit 全系统（地铁+公交+辅助客运）约 19 亿人次 |
| NY-D3 | 地铁工作日日均客流 | 2026 年 9 月：超过 420 万人次；2025 全年工作日均值为 2019 年水平的 74% | 2026-09 / 2025 | 月度工作日平均 | Office of Governor Hochul — https://www.governor.ny.gov/news/governor-hochul-and-mta-announce-billionth-subway-rider-2026；NYS Comptroller (OSC) — https://www.osc.ny.gov/press/releases/2026/04/dinapoli-mta-weekend-ridership-recovery-outpaces-weekdays-across-board | 官方 | 2025 全年工作日日均的绝对数未找到 |
| NY-D4 | 地铁单程票价 | $3.00（优惠票 $1.50；单程票卡 $3.50） | 2026-01-04 起 | 地铁/本地公交基础票价 | NYC311 — https://portal.311.nyc.gov/article/?kanumber=KA-01014；NYC Office of Payroll Administration — https://www.nyc.gov/site/opa/commuters/commuters.page | 官方 | 此前为 $2.90 |
| NY-D5 | 30 天无限次票价格 | 已取消；改为 OMNY 7 天封顶 $35（付满 12 次后免费） | 2026 | MetroCard 已于 2025-12-31 停售，30 天票随之停止（AirTrain JFK 除外） | NYC311（同上）；NYC OPA（同上，通勤福利月扣款由 $132 调为 $140 以覆盖 7 天封顶） | 官方 | 2022 参考值 $127 已无对应产品，比较时请改用“7 天 $35 / 月约 $140” |
| NY-D6 | 交通支出占家庭支出比重（BLS CE，纽约都会区） | 2023-24 占比 NOT FOUND；2023-24 户均总支出 $91,520；最近一份可读的占比为 2020-21 年的 11.7%（全国 16.2%） | 2023-24 / 2020-21 | BLS Consumer Expenditure Survey，NY-NJ-PA 都会区 | BLS — https://www.bls.gov/regions/northeast/news-release/consumerexpenditures_newyork.htm；2020-21 — https://www.bls.gov/regions/northeast/news-release/2022/consumerexpenditures_newyork_20221201.htm | 官方（取自搜索摘要） | bls.gov 正文被拦截，2023-24 占比请手动打开页面补录 |
| NY-E1 | NYC 官方贫困率（ACS） | 18.0% | 2024 | Census 官方贫困线，个人贫困率（ACS 2024 一年期） | NYC RGB 2026 I&A Study（引用 ACS 2024）— https://rentguidelinesboard.cityofnewyork.us/wp-content/uploads/2026/04/2026-IA.pdf | 官方（市政转引 Census） | 比 2023 年 −0.2 个百分点；全国为 12.1% |
| NY-E2 | 布朗克斯官方贫困率（ACS） | 28.8% | 2024 | 同上，Bronx County | 同上 | 官方（市政转引 Census） | 五区最高；布鲁克林 19.2%，曼哈顿 15.6% |
| NY-E3 | NYC Government Poverty Measure（NYCgov 贫困率） | 24.3%（2023 年为 23.1%，2022 年为 21.0%） | 2024 | 本地化贫困线（2024 年两大人两小孩家庭为 $51,978），计入税收和福利；2020-24 ACS PUMS 经 NYC Opportunity 加工 | NYC Opportunity, NYC Poverty Atlas — https://povertyatlas.nyc.gov/findings/key-poverty-trends-in-new-york-city-2023-2024/（发布于 2026-09-21） | 官方 | 数值取自页面图表数据。另一篇 2022 专题写的是 20.5%，属于修订前的数字。近贫（<150%）约一半，深度贫困（<50%）为 7% |
| NY-E4 | DHS 庇护所人数（最新月度） | 84,908 人（2026 年 3 月日均：有孩家庭 54,746 + 成人家庭 4,899 + 单身成人 25,263） | 2026-03 | DHS 月平均日人数，仅 DHS 系统，不含 HPD/HRA/DYCD/HERRC | NYC DHS, FY26 Data Dashboard — https://www.nyc.gov/assets/dhs/downloads/pdf/dashboard/tables/FY26-DHS-Data-Dashboard-Data.pdf | 官方 | 表中未注明是否含寻求庇护者。FY26 比 FY25 大幅上升（有孩家庭 +50%），疑似口径变化，见“可疑”清单。DHS 每日报告无法读取 |
| NY-E5 | DHS 年均庇护所人数及寻求庇护者部分 | 2025 年均 85,645 人（含寻求庇护者）；不含寻求庇护者为 57,249 人 → 寻求庇护者约 28,400 人（推算） | 2025 | DHS 每晚平均人数 | NYC RGB 2026 I&A Study（引用 NYC DHS）— https://rentguidelinesboard.cityofnewyork.us/wp-content/uploads/2026/04/2026-IA.pdf | 官方（市政转引 DHS） | 含寻求庇护者 −1.7%，不含 +2.1%。另据 NYC Comptroller：截至 2025-09-28，City 资助的各类庇护所中约有 33,300 名寻求庇护者（https://comptroller.nyc.gov/services/for-the-public/accounting-for-asylum-seeker-services/asylum-seeker-census/，取自搜索摘要） |
| NY-E6 | HUD PIT 无家可归者总数（NY-600 NYC CoC） | 125,683 人 | 2025（统计日 2025-01-28） | 一夜点数：紧急庇护所 118,160 + 过渡住房 2,850 + 露宿 4,673 | HUD Exchange, CoC Homeless Populations and Subpopulations NY-600 2025 — https://files.hudexchange.info/reports/published/CoC_PopSub_CoC_NY-600-2025_NY_2025.pdf | 官方 | 2024 年为 140,134 人（https://files.hudexchange.info/reports/published/CoC_PopSub_CoC_NY-600-2024_NY_2024.pdf） |
| NY-E7 | HUD PIT 露宿（unsheltered）人数 | 4,673 人 | 2025 | 同上 | 同 NY-E6 | 官方 | 2024 年为 4,397 人 |

## (1) NOT FOUND / 可疑清单（附已查来源）

- NY-B3 都会区家庭收入中位数（ACS 2024）：Census ACSBR-025 页面（https://www.census.gov/library/publications/2025/acs/acsbr-025.html）、www2.census.gov 上的 PDF、api.census.gov、data.census.gov 全部 403 或超时；只有聚合站 Census Reporter 有数（$99,155），不合规。
- NY-C6 都会区自有住房率：Census CPS/HVS 75 大 MSA 表（https://www.census.gov/housing/hvs/data/rates.html）403；FRED 只有州级数据。
- NY-D6 2023-24 交通支出占比：bls.gov 正文 403，搜索摘要里只有总额 $91,520。
- NY-A4 CSA（约 2,300 万口径）2025 年官方值：Census CBSA/CSA-EST2025 表 403，只在 Wikipedia 看到，不采用。
- NY-D3 2025 全年工作日日均的绝对人次：MTA ridership 页面 403，只找到“相当于 2019 年 74%”和 2026 年 9 月“超过 420 万”。
- NY-E4 可疑：FY26 DHS Dashboard 的有孩家庭人数同比 +50%、+24%，和 RGB 所说“2025 年总量 −1.7%”对不上，很可能是 FY26 起把原 HERRC 寻求庇护者家庭并入 DHS 统计。DHS 每日报告（a860-gpp.nyc.gov）和 NYC Open Data k46n-sa2m 均 403，无法核对最新日数。
- NY-D1 可疑/待核：472 座车站、约 250 英里线路、650+ 英里轨道均取自市政府页面，不是 MTA 原文；mta.info 403。
- NY-A2：2020 普查值 8,804,190 只在非官方转载中直接看到；官方摘要显示的是估算基数 8,805,594。
- 通用提醒：Census 2025 ACS 一年期数据可能已于 2026 年 9 月发布，但 census.gov 在本环境无法访问，所以 B2、C2–C4、E1、E2 用的是 RGB 所引的 2024 年版。建议手动打开 data.census.gov 查一下有没有 2025 年值。

## (2) 适合截图的官方页面（≤8）

1. NYC HPD 2026 AMI 表 — https://www.nyc.gov/site/hpd/services-and-information/area-median-income.page
2. NYC Poverty Atlas（NYCgov 贫困率 2022–2024 图表）— https://povertyatlas.nyc.gov/findings/key-poverty-trends-in-new-york-city-2023-2024/
3. NYC DHS Stats & Reports / Data Dashboard — https://www.nyc.gov/site/dhs/about/stats-and-reports.page
4. HUD 2025 PIT NY-600 报告 — https://files.hudexchange.info/reports/published/CoC_PopSub_CoC_NY-600-2025_NY_2025.pdf
5. NYC RGB 2026 Income & Affordability 简报（租金负担、贫困率、DHS 图）— https://rentguidelinesboard.cityofnewyork.us/wp-content/uploads/2026/04/2026-IA-Presentation.pdf
6. NYC HPD 2023 NYCHVS Selected Initial Findings — https://www.nyc.gov/assets/hpd/downloads/pdfs/about/2023%20NYCHVS%20Selected%20Initial%20Findings.pdf
7. NYC311 地铁/公交票价页（$3、7 天 $35）— https://portal.311.nyc.gov/article/?kanumber=KA-01014
8. Governor Hochul / MTA 2026 年第 10 亿名乘客公告（工作日客流）— https://www.governor.ny.gov/news/governor-hochul-and-mta-announce-billionth-subway-rider-2026
