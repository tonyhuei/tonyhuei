use "D:\政大課務處理\因果推論\期末報告資料\w3s_score.dta" 
merge 1:1 stud_id using "D:\政大課務處理\因果推論\期末報告資料\w3_sf_ct_cpnp_by_student_lv7.0.dta" 
drop _merge
merge 1:1 stud_id using "D:\政大課務處理\因果推論\期末報告資料\w3_sf_ctc_cpnp_by_student_lv7.0.dta" 
drop _merge
merge 1:1 stud_id using "D:\政大課務處理\因果推論\期末報告資料\w3_sf_dt_cpnp_by_student_lv7.0.dta" 
drop _merge
merge 1:1 stud_id using "D:\政大課務處理\因果推論\期末報告資料\w3_sf_dtc_cpnp_by_student_lv7.0.dta" 
drop _merge
merge 1:1 stud_id using "D:\政大課務處理\因果推論\期末報告資料\w3_sf_et_cpnp_by_student_lv7.0.dta" 
drop _merge
merge 1:1 stud_id using "D:\政大課務處理\因果推論\期末報告資料\w3_sf_etc_cpnp_by_student_lv7.0.dta" 
drop _merge
merge 1:1 stud_id using "D:\政大課務處理\因果推論\期末報告資料\w3_sf_mt_cpnp_by_student_lv7.0.dta" 
drop _merge
merge 1:1 stud_id using "D:\政大課務處理\因果推論\期末報告資料\w3_sf_mtc_cpnp_by_student_lv7.0.dta" 
drop _merge
merge 1:1 stud_id using "D:\政大課務處理\因果推論\期末報告資料\w3_sf_p_cpnp_lv7.0.dta" 
drop _merge
merge 1:1 stud_id using "D:\政大課務處理\因果推論\期末報告資料\w3_sf_s_cpnp_lv7.0.dta" 
drop _merge
merge 1:1 stud_id using "D:\政大課務處理\因果推論\期末報告資料\w3_sf_sev_cpnp_lv7.0.dta" 
drop _merge
merge 1:1 stud_id using "D:\政大課務處理\因果推論\期末報告資料\w4_sf_ct_cpnp_by_student_lv7.0.dta" 
drop _merge
merge 1:1 stud_id using "D:\政大課務處理\因果推論\期末報告資料\w4_sf_ctc_cpnp_by_student_lv7.0.dta" 
drop _merge
merge 1:1 stud_id using "D:\政大課務處理\因果推論\期末報告資料\w4_sf_dt_cpnp_by_student_lv7.0.dta" 
drop _merge
merge 1:1 stud_id using "D:\政大課務處理\因果推論\期末報告資料\w4_sf_dtc_cpnp_by_student_lv7.0.dta" 
drop _merge
merge 1:1 stud_id using "D:\政大課務處理\因果推論\期末報告資料\w4_sf_et_cpnp_by_student_lv7.0.dta" 
drop _merge
merge 1:1 stud_id using "D:\政大課務處理\因果推論\期末報告資料\w4_sf_etc_cpnp_by_student_lv7.0.dta" 
drop _merge
merge 1:1 stud_id using "D:\政大課務處理\因果推論\期末報告資料\w4_sf_mt_cpnp_by_student_lv7.0.dta" 
drop _merge
merge 1:1 stud_id using "D:\政大課務處理\因果推論\期末報告資料\w4_sf_mtc_cpnp_by_student_lv7.0.dta" 
drop _merge
merge 1:1 stud_id using "D:\政大課務處理\因果推論\期末報告資料\w4_sf_p_cpnp_lv7.0.dta" 
drop _merge
merge 1:1 stud_id using "D:\政大課務處理\因果推論\期末報告資料\w4_sf_s_cpnp_lv7.0.dta" 
drop _merge
merge 1:1 stud_id using "D:\政大課務處理\因果推論\期末報告資料\w4_sf_sev_cpnp_lv7.0.dta" 
drop _merge
replace w4sch_id= w3sch_id if w4sch_id==""
merge m:m w4sch_id using "D:\政大課務處理\因果推論\期末報告資料\w4_sf_sch_lv7.0.dta" 
drop _merge
drop if w4clspgm >=40& w4clspgm!=48
order w4clspgm
inspect g_total indrg if w4clspgm==21
inspect g_total indrg if w4clspgm==22
inspect g_total indrg if w4clspgm==23
inspect g_total indrg if w4clspgm==31
inspect g_total indrg if w4clspgm==32
inspect g_total indrg if w4clspgm==48
inspect indrs if w4clspgm==21
inspect indrs if w4clspgm==22
inspect indrs if w4clspgm==23
inspect indrs if w4clspgm==31
inspect indrs if w4clspgm==32
inspect indrs if w4clspgm==48
tab indrs if w4clspgm==21&s1==0&s2==0&s3==0&s4==0
tab indrs if w4clspgm==22&s1==0&s2==0&s3==0&s4==0
tab indrs if w4clspgm==23&s1==0&s2==0&s3==0&s4==0
tab indrs if w4clspgm==31&s1==0&s2==0&s3==0&s4==0
tab indrs if w4clspgm==32&s1==0&s2==0&s3==0&s4==0
tab indrs if w4clspgm==48&s1==0&s2==0&s3==0&s4==0
drop if indrg==.& indrs==.
drop if indrg==0& indrs==0
drop if indrg==0
drop if g_total==0
drop chinese english matha mathb mathc w4s4634 w4s4635 w4s4636 w4s4641 w4s4642 w4s4643 w4s4644 w4s4651 w4s4652 w4s4653 w4s4654 w4s4655 w4s4656 w4s4661 w4s4662 w4s4663 w4s4664 ///
 w4s4671 w4s4672 w4s4673 w4s4674 w4s4701 w4s4702 w4s4703 w4s4704 w4s471 w3log1 w3log2 w3log3 w3log4 w3log5 w3log6 w3log7 w3log8 w3log9 w3log10 w3log11 w3log12 w3log13 w3log14 ///
 w3log15 w3p115 w3p116 w3p117 w3p118 w3p120 w3p203 w3p204 w3p213 w3p214 w3p302 w3p303 w3p3042 w3p3044 w3p3045 w3p3046 w3p4051 w3p404 w3p4052 w3p4053 w3p4054 w3p4055 w3p4056 ///
 w3p4081 w3p4082 w3p4083 w3p4084 w3p4085 w3p4086 w3p4151 w3p4154 w3p4155 w3p4291 w3p4292 w3p4293 w3p4294 w3p4295 w3p4296 w3p722 w3p721 w3p723 w3p724 w3p726 w3fatwn w3fahak w3faabr ///
 w3fajap w3mochn w3motwn w3mohak w3moabr w3mojap w4log14 w4log15 w4log16 w4log17 w4log18 w4log19 w4log20 w4log21 w4log22 w4log23 w4log24 w4log25 w4log26 w4log27 w4log28 w4log29 ///
 w4log30 w4log31 w4log32 w4log33 w4log34 w4log35 w4log36 w4log37 w4log38 w4log39 w4log40 w4log41 w4log42 w4log43 w4log44 w4log45 w4log46 w4log47 w4h1035 w4h107 w4h108 w4h109 ///
 w4h1151 w4h1152 w4h1153 w4h1154 w4h1155 w4h1156 w4h144 w4h146 w4h148 w4h149 w4h150 w4h3461 w4h3462 w4h3463 w4h3464 w4h3465 w4h3491 w4h3492 w4h3493 w4h3494 w4h3495 w4h3501 w4h3502 ///
 w4h3503 w4h3504 w4h390 w4h6264 w4h631 w4h632 w4h633 w4h634 w3s408 w3s414 w3s450 w3s451 w3s452 w3s453 w3s4571 w3s4573 w3s4575 w3s4572 w3s469 w3s471 w3s497 w3s495 w3log19 w3log20 ///
 w3log21 w3log22 w3log23 w3log24 w3log25 w3log26 w3log27 w3log28 w3log29 w3log30 w3td04 w3td05 w3td14 w3td15 w3td16 w4t3144 w4t3145 w4t4224 w4t4225 w4log1 w4log2 w4log3 w4log4 ///
 w4log5 w4log6 w4log7 w4log8 w4log9 w4log10 w4log11 w4log12 w4log13 w4h6232 w4h6233 w4h6234 w4h6235 w4h6236 w4h6241 w4h6242 w4h6243 w4h6244 w4h6245 w4h6246 w4h417 w4h3481 w4h3482 ///
 w4h3483 w4h3484 w4h3485 w4h3505 w4h3291 w4h3292 w4h3293 w4h3294 w4h3301 w4h3302 w4h3303 w4h3304 w4s4771 w4s4772 w4s4773 w4s4781 w4s4783 w4s4691 w4s4692 w4s4681 w4s4682 w4s4631 ///
 w4s4632 w4s4633 w4s4621 w4s4622 w4s4623 w4s4624 w4s4625 w4s4626 w4s3331 w4s3332 w4s3321 w4s3322 w4s3301 w4s3302 w4s3311 w4s3312 w4s3062 w4s2191 w4s2192 w4s2193 w4s2194 w4s2196 ///
 w4s220 w4s2141 w4s2142 w4s2143 w4s2131 w4s2132 w4s2133 w4s2122 w4s2123 w4s2124 w4s2102 w4s2103 w4s2104 w4s2092 w4s2093 w4s2094 w4s2082 w4s2083 w4s2084 w4s2072 w4s2073 w4s2074 ///
 w4s2062 w4s2063 w4s2064 w4s124 w4s123 w4s125 w4s126 w4s127 w4s121 w4s122 w4s3072 w4s3061 w4h638 w4h641 w4h3281 w4h3282 w4h3283 w4h3284 w4h3471 w4h3472 w4h3473 w4h3474 w4h3475 ///
 w4h406 w4h405 w4s4782 w4s443 w4s429 w4s2281 w4s2282 w4s2283 w4s2284 w4s2285 w4s2286 w4s2301 w4s2302 w4s2303 w4s2304 w4s2305 w4s2306 w4s2311 w4s2312 w4s2313 w4s2314 w4s2315 ///
 w4s2316 w4s2361 w4s2362 w4s2363 w4s2364 w4s2365 w4s2366 w4s2251 w4s2252 w4s2253 w4s2254 w4s2255 w4s2256 w4s2241 w4s2242 w4s2243 w4s2244 w4s2245 w4s2246 w4s1334 w4s1333 w4s1332 ///
 w4s1331 w4p508 w4p5095 w4p5101 w4p5102 w4p5103 w4p5104 w4p5105 w4p511 w4p512 w4p515 w4p516 w4p517 w4p519 w4p520 w4p521 w4p522 w4p524 w3t1231 w3t1232 w3t1233 w3t1234 w3t1235 ///
 w3t1236 w3t1241 w3t1242 w3t1243 w3t1244 w3t1245 w3t1246 w3t1154 w3t1155 w3ctc41 w3dtc12 w3dtc10 w3dtc15 w3dtc17 w3dtc18 w3dtc19 w3dtc16 w3etc41 w3mtc41 w3p123 w3p202 w3p210 ///
 w3p211 w3p215 w3p3063 w3p3065 w3p310 w3p4144 w3p5014 w3p5013 w3p5012 w3p5011 w3p503 w3p5041 w3p5042 w3p5043 w3p5044 w3p5045 w3p5046 w3p505 w3p506 w3p5071 w3p5072 w3p5073 w3p5074 ///
 w3p5075 w3p5076 w3p508 w3p509 w3p5101 w3p5102 w3p5103 w3p5104 w3p5105 w3p5106 w3p511 w3p523 w3p5261 w3p5262 w3p5271 w3p5272 w3p5293 w3p533 w3p531 w3log16 w3log17 w3log18 w3s115 ///
 w3s116 w3s117 w3s118 w3s119 w3s120 w3s135 w3s138 w3s139 w3s140 w3s141 w3s201 w3s202 w3s204 w3s206 w3s207 w3s208 w3s209 w3s210 w3s2181 w3s2194 w3s2193 w3s2192 w3s2191 w3s220 ///
 w3s2211 w3s2212 w3s2213 w3s2214 w3s3021 w3s3022 w3s3023 w3s3024 w3s3025 w3s3026 w3s3312 w3s3313 w3s3314 w3s3316 w3s332 w3s333 w3s334 w3s335 w3s336 w3s337 w3s413b w3s429 w3s431 ///
 w3s432 w3s433 w3s439 w3s440 w3s442 w3s447 w3s448 w3s449 w3s461 w3s470 w3td13 w4t204 w4t205 w4t206 w4t207 w4t208 w4t209 w4t210 w4t211 w4t212 w4t213 w4t433 w4p2142 w4p2145 w4p2152 ///
 w4p2153 w4p2154 w4p2155 w4p221 w4p222 w4p2331 w4p2332 w4p5106 w4p5096 w4s119 w4s117 w4s118 w4s1371 w4s1372 w4s202 w4s203 w4s2041 w4s2042 w4s2043 w4s2044 w4s2045 w4s2046 w4s216 ///
 w4s217 w4s218 w4s2211 w4s2212 w4s2213 w4s2214 w4s2215 w4s2221 w4s2222 w4s2223 w4s2224 w4s2225 w4s2226 w4s2261 w4s2262 w4s2263 w4s2264 w4s2265 w4s1361 w4s1362 w3p5292 ///
 w4h387an w4h387bn w4h388an w4h388bn w4h635 w4h636 w4h637 w4h639 w4h640 w4h6272 w4h6271 w4h6164 w4h6163 w4h6162 w4h6161 w4h6152 w4h6153 w4h6154 w4h6155 w4h6156 w4h505 w4h506 ///
 w4h507 w4h503 w4h3451 w4h3452 w4h3453 w4h3454 w4h3455 w4h2561 w4h2562 w4h2563 w4h2564 w4h2565 w4h2566 w4h257 w4h2581 w4h2582 w4h2583 w4h2584 w4h2585 w4h2586 w4h234 w4h235 w4h236 ///
 w4h237 w4h238 w4h239 w4h240 w4h241 w4h242 w4h243 w4h183a w4h183an w4h183b w4h183bn w4h119 w4h121 w4h122 w4h123 w4h124 w4h125 w4h126 w4s4613 w4s423 w4s422 w4s421 w4s420 w4s3371 ///
 w4s3372 w4s3373 w4s3374 w4s3375 w4s3381 w4s3382 w4s3383 w4s3384 w4s2291 w4s2292 w4s2293 w4s2294 w4s2295 w4s2296 w4s2266 w4p305 w4p306 w4p307 w4p308 w4p309 w4p310 w4p311 w4p312 ///
 w4p313 w4h6011 w4h6012 w4h6013 w4h6014 w4h6015 w4h6016 w4h6021 w4h6022 w4h6023 w4h6024 w4h6025 w4h6026 w4h6141 w4h6142 w4h6143 w4h6144 w4h6151 w4h6165 w4h619 w4h620 w4h621 w4h622 ///
 w4h6261 w4h6262 w4h6263 w4h6265 w4h629 w4h630 w4h5111 w4h5112 w4h5113 w4h5114 w4h5115 w4h5116 w4h512 w4h510 w4h5011 w4h5012 w4h5013 w4h5014 w4h5015 w4h5016 w4h502 w4h504 w4h508 ///
 w4h401 w4h402 w4h201 w4h202 w4h203 w4h204 w4h205 w4h374 w4h375 w4h376 w4h377 w4h4041 w4h4042 w4h4043 w4h4044 w4h4045 w4h211 w4h212 w4h213 w4h244 w4h245 w4h246 w4h247 w4h248 w4h1032 /// 
 w4h1033 w4h1034 w4h1036 w4swt1 w4h101 w4h102 w4h104 w4h112a w4h112b w4h113 w4h114 w4h116 w4h117 w4h118 w4h127 w4h128 w4h129 w4h130 w4h131 w4h132 w4h133 w4h134 w4h135 w4h136 w4h137 ///
 w4h139 w4h138 w4h140 w4h110 w4h106 w4h143 w4h311 w4h301b w4h320b w4h321a w4h321b w4h322a w4h322b w4h408 w4h411 w4h412 w4h5091 w4h5092 w4h5093 w4h5094 w4h5095 w4h5096 w4s424 w4s425 ///
 w4s426 w4s427 w4s428 w3t101 w3t102 w3t103 w3t104 w3t105 w3t106 w3t110 w3t111 w3t1121 w3t1122 w3t1124 w3t1125 w3t1126 w3t1131 w3t1132 w3t1133 w3t1134 w3t1135 w3t1136 w3t114 w3t1152 ///
 w3t1161 w3t1162 w3t1163 w3t1164 w3t1165 w3t1166 w3t117 w3t118 w3t119 w3t120 w3t121 w3t1221 w3t1222 w3t1223 w3t1224 w3t1225 w3t1226 w3t1251 w3t1252 w3t1253 w3t1254 w3t1255 w3t1256 ///
 w3t2151 w3t2152 w3t2153 w3t2154 w3t2155 w3t2156 w3t217 w3t218 w3t2191 w3t2192 w3t2193 w3t2194 w3t2195 w3t2196 w3t220 w3t314 w3t315 w3t320 w3t321 w3t322 w3t325 w3sumerr w3summis ///
 w3sumlog w3ctc03 w3dtc11 w3mtc03 w3p105 w3p108 w3p109 w4s401 w4s403 w4s404 w3t1123 w3t1151 w3t1153 w3t1156 w3t201 w3t202 w3t203 w3t204 w3t205 w3t206 w3t207 w3t208 w3t209 w3t2131 ///
 w3t2132 w3t2133 w3t2134 w3t2135 w3t2136 w3t214 w3t402 w3t403 w3t4064 w3t4065 w3t4066 w3t407 w3t4101 w3t4102 w3t4103 w3t4104 w3t4105 w3t4106 w3ctc04 w3stwt1 w3all3ps w3cf3ps w3ctc38 /// 
 w3ctc39 w3dtch_id w3dtc01 w3dtc02 w3dtc04 w3dtc05 w3dtc06 w3dtc07 w3engl_id w3etch_id w3etc01 w3etc02 w3etc03 w3etc15 w3etc38 w3etc39 w3math_id w3mtch_id w3mtc01 w3mtc02 w3mtc38 ///
 w3mtc39 cp w3p101 w3p102 w3p103 w3p106 w3p112 w3p113  w3p128 w3p206 w3p301 w3p4141 w3p4142 w3p4143 w3p4145 w3p4146 w3p4152 w3p4153 w3p4156 w3p428 w3p432  w3p5274 w3p5273 w3p5264 ///
 w3p5263 w3p518 w3p519 w3p521 w3p522 w3p528 w3p5291 w3p6071 w3p6072 w3p6073 w3p6074 w3p6075 w3p6076 w3p702 w3p703 w3p704 w3p7151 w3p7152 w3p7153 w3p7154 w3p7155 w3p7156 w3p716 w3p717 ///
 w3p718 w3p608 w3p609 w3p610 w4p101 w4p102 w4p103 w4p106 w4p118 w4p119 w4p120 w4p121 w4p122 w4p123 w4p224 w4p223 w4p240 w4p301 w4p403 w4p402 w4p405 w4p406 w4p428 w4p429 w4p430 w4p431 ///
 w4p433 w4p434 w4p435 w4p501 w4p502 w4p503 w4p504 w4p505 w4p506 w4p507 w4p5091 w4p5092 w4p5093 w4p5094 w4p513 w4p514 w4p518 w4p523 w4p525 w4parent w4spouse w3scarea w3admarea ///
 w3cls_pn w3maler w3t408 w3t409 w3t4111 w3t4112 w3t4113 w3t4114 w3t4115 w3t4116 w3ctc01 w3ctc02 w4t101 w4t102 w4t103 w4t104 w4t107 w4t108 w4t109 w4t110 w4t114 w4t116 w4t117 w4t118 ///
 w4t119 w4t120 w4t121 w4t122 w4t123 w4t2011 w4t2012 w4t2013 w4t2014 w4t2015 w4t2016 w4t2021 w4t2022 w4t2023 w4t2024 w4t2025 w4t2031 w4t2032 w4t2033 w4t2034 w4t2035 w4t2036 w4t214 ///
 w4t215 w4t222 w4t221 w4t225 w4t227 w4t229 w4t230 w4t231 w4t232 w4t301 w4t302 w4t303 w4t304 w4t305 w4t306 w4t307 w4t308 w4t309 w4t310 w4t3141 w4t3142 w4t3143 w4t3146 w4t401 w4t402 ///
 w4t403 w4t4041 w4t4042 w4t4043 w4t4044 w4t4045 w4t4046 w4t4051 w4t4052 w4t4053 w4t4054 w4t4055 w4t4056 w4t4061 w4t4062 w4t4063 w4t4064 w4t4071 w4t4072 w4t4073 w4t4074 w4t4075 w4t4076 ///
 w4t408 w4t409 w4t410 w4t411 w4t412 w4t413 w4t416 w4t417 w4t418 w4t419 w4t420 w4t4211 w4t4212 w4t4213 w4t4214 w4t4215 w4t4216 w4t4221 w4t4222 w4t4222 w4t4223 w4t4226 w4t4231 w4t4232 w4t4233 ///
 w4t4234 w4t4235 w4t4236 w4t424 w4sumerr w4summis w4sumtrp w4sumlog w4dtc04 w4dtc05 w4dtc06 w4dtc07 w4dtc09 w4dtc10 w4dtc12 w4etc01 w4mtc01 w4mtc02  w4s4611 w4s4612 w4s4614 w4s4615 w4s4616 ///
 w4td01 w4td02 w4td04 w4td08 w4sx01 w4sx02 w4s4775 w4s4785 w4s4684 w4s4694 w4s431 w4s301 w4s302 w4s303 w4s304 w4s3064 w4s3065 w4s3074 w4s3075 w4s308 w4s309 w4s310 w4s311 w4s312 w4s313 ///
 ind42 w3s222 w3s301 w3s303 w3s304 w3s305 w3s306 w3s316 w3s314 w3s3181 w3s3183 w3s3184 w3s3185 w3s3186 w3s319 w3s321 w3s323 w3s3251 w3s3253 w3s3254 w3s3255 w3s3256 w3s326 w3s3311 w3s345 ///
 w3s346 w3s347 w3s348 w3s349 w3s4191 w3s4192 w3s4193 w3s4194 w3s4195 w3s454 w3s455 w3s456 w3s4576 w3s458 w3s459 w3s462 w3s463 w3s464 w3s466 w3s468 w3s479 w3s5011 w3s5012 w3s5013 w3s5014 ///
 w3s5015 w3s5016 w3td01 w3td02 w3td10 w3td11 w3td12 w3t303 w3t306 w3t307 w3t308 w4s131 w3p3041 w3p3043 w3p305 w3p3061 w3p3062 w3p3064 w3p3066 w3p307 w3p312 w3p313 w3p314 w3p315 w3p316 w3p317 ///
 w3p318 w3p319 w3p401 w3p308 w3p309 w3p311 w3faethn w3fachn w3fawfor w3facoll w3fasdep w3fatest w3fawlic w3fanei w3famemb w3fabyr w3famana w3moethn w3mowfor w3mocoll w3mosdep w3motest /// 
 w3mowlic w3moplic w3monei w3momemb w3mobyr w3sumtrp w3s112 w3s133 w3s137 w3s145 w3s146 w3s148 w3s149 w3s1571 w3s1572 w3s1574 w3s1576 w3s203 w3s205 w3s211 w3s215 w3s216 w3s217 w3s2184 w3s2186 ///
 w3s350 w3s351 w3s352 w3s353 w3s354 w3s355 w3s356 w3s357 w3s358 w3s359 w3s360 w3s361 w3s362 w3s401 w3s402 w3s410b w4s1085 w4s1125 w3t301 w3t302 w3t304 w3t305 w3t324 w3ctc07 w3ctc08 w3ctc13 ///
 w3ctc14 w3ctc15 w3ctc18 w3ctc19 w3ctc28 w3ctc29 w3etc28 w3etc29 w3mtc13 w3mtc14 w3mtc15 w3mtc26 w3mtc27 w3mtc25 w3mtc28 w3mtc29 w3s483 w3s499 w3s500 w4s415 w4s417 w4s418 w4s419 w4s416 ///
 w4s1084 w4s1086 w4s1124 g4a g5a g_total s1 s2 s3 s4 w3t309 w3t310 w3t312 w3t313 w3t318 w3t323 w3t404 w3t405 w3t4061 w3t4062 w3etc07 w3etc08 w3etc13 w3etc14 w3etc18 w3etc19 w3mtc04 w3mtc07 /// 
 w3mtc08 w3s102 w3s103 w3s108 w3s109 w3s110 w3s113 w3s122 w3s123 w3s1301 w3s1303 w3s1304 w3s1305 w3s1306 w3s131 w3s212 w3s2195 w3s310 w3s311 w3s312 w3s344 w3s465 w3s446 w4stwt1 w4stwt2 w4all3ps ///
 w4cf3ps w4m3ps w4t223 w4t220 w4t218 w4t224 w4t226 w4t312 w4t313 w4ctc01 w4ctc02 w4t434 w4t435 w4t436 w4t432 w4t431 w4t430 w4t429 w4ctc10 w4ctc11 w4ctc16 w4ctc18 w4ctc19 w4ctc20 w4ctc21 w4ctc22 ///
 w4ctc23 w4ctc26 w4ctc27 w4etc02 w4etc03 w4etc11 w4etc16 w4etc17 w4etc18 w4etc19 w4etc20 w4etc21 w4etc22 w4etc23 w4etc26 w4etc27 w4mtc10 w4mtc11 w4mtc16 w4mtc17 w4mtc18 w4mtc19 w4mtc20 w4mtc21 ///
 w4mtc22 w4mtc23 w4mtc27 w4p112 w4p113 w4p114 w4p220 w4p2452 w4p2453 w4p2454 w4p2455 w4p314 w4p3201 w4p3202 w4p3203 w4p3204 w4p3205 w4p3206 w4p4251 w4p4252 w4p4253 w4p4254 w4p4255 w4p4256 w4p426 ///
 indrg w3nright w3cfree w3math w3m3ps w3t107 w4h407 w4h409 w4h141 w4h142 w4s405 w4s406 w4s3216 w4s3215 w4s3214 w4s3213 w4s3212 w4s3211 w4s320 w4s2321 w4s2322 w4s2323 w4s2324 w4s2325 w4s2326 w4s2341 ///
 w4s2342 w4s2343 w4s2344 w4s2345 w4s2346 w4s2351 w4s2352 w4s2353 w4s2354 w4s2355 w4s2356 w4s2112 w4s2113 w4s2114 w4s1351 w4s1352 w4s1353 w4s1363 w4s1364 w4s1365 w4s1366 w4s1373 w4s138 w4s139 w4s140 ///
 w4s141 w4s201 w4s205 w4s101 w4fahlth w4mohlth w4h6257 w3sx03 w3sx04 w3sx05 w3s478 w4s305 w4s3063 w4s3066 w4s3071 w4s3073 w4s3076 w4s2336 w4s472 w4s473 w4s474 w4s475 w4s476 w4s3306 w4s3316 w4s3326 ///
 w4s3266 w4s2121 w4s2135 w4p303 w4p302 w3sx01 w3sx02 w3p1111 w3p1112 w3p1113 w3p1114 w3p1115 w3p1116 w3p601  w3p122 w3p124 w3p502 w3p525 w3s1302 w3s132 w3s134 w3s136 w3s487 w3s488 w3s490 w4ctc326 ///
 w4dtc156 w4etc326 w4mtc326 w4p210 w4p211 w4p212 w4p2144 w4p213 w4p2156 w4p216 w4p227 w4p228 w4s3323 w4s3324 w4s3325 w4s408 w4s410 w3p5015 w3s2215 w3s2216 w3s363 w3s403 w3s4201 w3s4202 w3s4203 w3s4204 ///
 w3s4205 w3s4206 w3p114 w4nright w4all3p w4cfree w4cf3p w4math w4m3p w3w4plus w3w4minus w4link w4illp w3m3p w3link w3ctc09 w3ctc10 w3ctc11 w3ctc12 w3ctc22 w3ctc23 w3ctc24 w3ctc25 w3ctc26 w3ctc27 ///
 w3etc09 w3etc10 w3etc11 w3etc12 w3etc22 w3etc23 w3etc24 w3etc25 w3etc26 w3etc27 w3mtc09 w3mtc10 w3mtc11 w3mtc12 w3mtc22 w3mtc23 w3mtc24 w4ctc12 w4ctc13 w4ctc14 w4ctc15 w4ctc17 w4etc10 w4etc12 w4etc13 ///
 w4etc14 w4etc15 w4mtc12 w4mtc13 w4mtc14 w4mtc15 w4mtc26 w3s364 w3s365 w3p603 w3p727 w3fawork w3faread w3faplic w3moread w3mowork w3momana w4t311 w4t414 w4t415 w4t425 w4t426 w4t427 w4t428 w4p111 w4p115 ///
 w4p201 w4p407 w4p408 w4p409 w3p205 w4p203 w3s127 w4s1146 w4s1155 w4s1156 w4s1151 w4s1136 w4h3633 w4s329 w4s3336 w4s334 w3s129 w4s2081 w4s2091 w4s2101 w4s2111 w4s2061 w4s2071 w4s2136 w4s2145 w4s2146 ///
 w4s2155 w4s2151 w4s2152 w4s2153 w3mtc37 w3all3p w3cf3p w3ctc37 w3ctc425 w3etc37 w3etc425 w3mtc425 w4ctc315 w4etc315 w4mtc315 w4p2336 w4p419 w4s120 w4h145 w3t401 w4ctc03 w4s1286 w4s1291 w4s1295 w4s1306 ///
 w4s1321 w4s1322 w4s1323 w4s1324 w4s1325 w4s1326 w4s1335 w4s1336 w4h312 w4h319b w3s2182 w3s2183 w3s2185 w3s2196 w4s2276 w4s2236 w4s2376 w3s3286 w4s2381 w4s2382 w4s2383 w4s2384 w4s2385 w4s2386 w4s4693 ///
 w4s4774 w4s4784 w3s481 w3s482 w3s484 w3s485 w3s486 w3s489 w3s491 w3s492 w3s493 w3s494 w3s496 w3s498 w3p119 w3p121 w3p125 w3p126 w3p127 w3p514 w3p515 w3p516 w3p517 w3p520 w3p524 w3p5294 w3p530 w3p532 ///
 w3p534 w3p535 w3p536 w4s2195 w4s2216 w4s2231 w4s2232 w4s2233 w4s2234 w4s2235 w4s2271 w4s2272 w4s2273 w4s2274 w4s2275 w4s2331 w4s2332 w4s2333 w4s2334 w4s2335 w4s2371 w4s2372 w4s2373 w4s2374 w4s2375 ///
 w4p315 w4p304 w3s142 w3s143 w3s144 w3s147 w3s150 w3s151 w3s152 w3s153 w3s154 w3s155 w3s156 w3s1573 w3s1575 w3tes1 w3tcs1 w3tms1 w4t105 w4dtc14 w4ctc05 w3faeng w3moeng w3p719 w3p720 w3p725 w4s430 ///
 w4sx03 w4sx04 w4sx05 w4s1126 w3s368 w3s366 w3s367 w4s414 w4p427 w4p432 w4p436 w4p437 w4s323 w4s3241 w4s3246 w4s3242 w4etc05 w4p415 w4p416 w4p417 w4p418 w4p420 w4p2451 w4p2456 w4s1354 w4s1355 w4s1356 ///
 w4s1374 w4s1375 w4s1376 w4s327 w4s3281 w4s3286 w4s2134 w4s2144 w4s2154 w4s2134 w4s2144 w4s2154 w4s4683 w4s109  w4mtc05 w4mtc04  w4s325 w4s3261 w4s2125 w4p238 w4p239 w4p241 w4p242 w3td09 w4s317 w4s316 ///
 w4s447 w4s448 w4s445 w4s446 w4s454 w4mtc30 w4etc30 w4ctc30 w3s430 w3s434 w3s435 w3s436 w3s437 w3s438 w3s441 w3s443 w3s444 w4t106 w4p235 w4p236 w4p116 w4p117 w4p244 w4p411 w3mtc18 w3mtc19 w4p410 w4p411 ///
 w4mtc08 w4etc08 w4ctc08 w4s134 w4s107 w3s114 w3s214 w3p706 w4s460 w4dtc01 w4mtc03  w3t216 w3td06 w3td03 w3s3182 w3s3252  w3t210 w3t211 w4t228 w3s128  w4t113 w4t115 w4t111  w4p237 w4p243 w4s318 w3s124 ///
 w3s125  w4p2151 w4ctc25 w4etc25 w4mtc25 w3t212 w4t112 w4t219 w3t319 w3ctc17 w3etc17 w3mtc17 w3etc04 w4ctc06 w4etc06 w4mtc06 w3s105 w4dtc02  w3s467 w3s107 w3s445 w3p207 w3p208 w4s116 w3t108 w3t109 ///
 
egen cramnum=rowtotal(w4s1081 w4s1082 w4s1083)
drop if cramnum==297
gen coretotal= g1a+g2a+g3a
replace w4faedu = . if w4faedu==99
replace w4moedu = . if w4moedu==99
gen wfaedu=1 if w4faedu==1
replace wfaedu=2 if w4faedu==2|w4faedu==3
replace wfaedu=3 if w4faedu==4|w4faedu==5
replace wfaedu=4 if w4faedu==6
gen wmoedu=1 if w4moedu==1
replace wmoedu=2 if w4moedu==2|w4moedu==3
replace wmoedu=3 if w4moedu==4|w4moedu==5
replace wmoedu=4 if w4moedu==6
replace wfaedu = wmoedu if wfaedu==.
replace wmoedu = wfaedu if wmoedu==.
gen paredu= (wfaedu+ wmoedu)/2
drop w3parent w3spouse w3faedu w3moedu w4p401 w4p104 w3p104
drop if w4sch_id=="047" //刪除同學的學校沒寫學校問卷
gen scenhan=w4h6251+w4h6252+w4h6253+w4h6254+w4h6255+w4h6256+w4h6258
replace scenhan=0 if scenhan==693
replace w4h388a=0 if w4h388a==9999
replace w4h388b=0 if w4h388b==9999
replace w4h388a=0 if w4h388a==9995
replace w4h388b=0 if w4h388b==9995
replace w4h387a=0 if w4h387a==9995
replace w4h387b=0 if w4h387b==9995
gen scunipub= (w4h387a +w4h388a)/( w4h387a+w4h387b+w4h388a+w4h388b)
replace scunipub=0 if scunipub==.
replace w4h6231=0 if w4h6231 ==99
label define w4h365 2 "各年級都有" 1 "部分年級有" 0 "都沒有" 97 "不合理值" 99 "遺漏值", replace
label define w4h364 2 "各年級都有" 1 "部分年級有" 0 "都沒有" 97 "不合理值" 99 "遺漏值", replace
label define w4h362 2 "各年級都有" 1 "部分年級有" 0 "都沒有" 1 "特殊情況" 97 "不合理值" 99 "遺漏值", replace
replace w4h365=0 if w4h365==3
replace w4h365=4 if w4h365==2
replace w4h365=2 if w4h365==1
replace w4h365=1 if w4h365==4
replace w4h364=0 if w4h364==3
replace w4h364=4 if w4h364==2
replace w4h364=2 if w4h364==1
replace w4h364=1 if w4h364==4
replace w4h362=0 if w4h362==3
replace w4h362=5 if w4h362==2
replace w4h362=2 if w4h362==1
replace w4h362=1 if w4h362==4
replace w4h362=1 if w4h362==5
replace w4h3273=2 if w4h3273==1
replace w4h3274=3 if w4h3274==1
gen scaward=w4h3272+w4h3273+w4h3274
replace w4h3631=3 if w4h3631==1
replace w4h3632=2 if w4h3632==1
gen schelpcla=w4h3631+w4h3632+w4h3634
gen scteamatt= w4s3333+ w4s3334+ w4s3335
drop w4s3333 w4s3334 w4s3335
gen outclubatt= w4s3303+w4s3304+w4s3305+w4s3313+w4s3314+w4s3315
drop w4s3303 w4s3304 w4s3305 w4s3313 w4s3314 w4s3315
gen beforecram= w4s1131+ w4s1132+ w4s1133+ w4s1141+ w4s1142+ w4s1143
gen ctclag2= w3ctc421+ w3ctc422+ w3ctc423+ w3ctc424+ w3ctc426
drop w3ctc421 w3ctc422 w3ctc423 w3ctc424 w3ctc426
gen ctclag3= w4ctc311+ w4ctc312+ w4ctc313+ w4ctc314+ w4ctc316
drop w4ctc311 w4ctc312 w4ctc313 w4ctc314 w4ctc316
gen etclag2= w3etc421+ w3etc422+ w3etc423+ w3etc424+ w3etc426
drop w3etc421 w3etc422 w3etc423 w3etc424 w3etc426
gen mtclag2= w3mtc421+ w3mtc422+ w3mtc423+ w3mtc424+ w3mtc426
drop w3mtc421 w3mtc422 w3mtc423 w3mtc424 w3mtc426
gen etclag3= w4etc311+ w4etc312+ w4etc313+ w4etc314+ w4etc316
drop w4etc311 w4etc312 w4etc313 w4etc314 w4etc316
gen mtclag3= w4mtc311+ w4mtc312+ w4mtc313+ w4mtc314+ w4mtc316
drop w4mtc311 w4mtc312 w4mtc313 w4mtc314 w4mtc316
replace ctclag2=. if ctclag2==495
replace mtclag2=. if mtclag2==495
replace etclag2=. if etclag2==495
replace ctclag3=. if ctclag3==495
replace etclag3=. if etclag3==495
replace mtclag3=. if mtclag3==495
replace ctclag2= ctclag3 if ctclag2==.
replace ctclag3= ctclag2 if ctclag3==.
replace mtclag2= mtclag3 if mtclag2==.
replace mtclag3= mtclag2 if mtclag3==.
replace etclag2= etclag3 if etclag2==.
replace etclag3= etclag2 if etclag3==.
gen ctclag= (ctclag2+ctclag3)/2
gen mtclag= (mtclag2+mtclag3)/2
gen etclag= (etclag2+etclag3)/2
gen teststre= w4s1281+w4s1282+w4s1283+w4s1284+w4s1285
replace teststre=. if teststre==495
gen stubestcl= w4s1152+ w4s1153+ w4s1154
replace stubestcl=. if stubestcl==297
gen cram12= w4s1134+ w4s1144
gen cram3= w4s1135+ w4s1145
gen freecram= w4s1121+ w4s1122+ w4s1123
gen ctcfor3= w4ctc321+ w4ctc322+ w4ctc323+ w4ctc324+ w4ctc325
gen etcfor3= w4etc321+ w4etc322+ w4etc323+ w4etc324+ w4etc325
gen mtcfor3= w4mtc321+ w4mtc322+ w4mtc323+ w4mtc324+ w4mtc325
gen dtcfor3= w4dtc151+ w4dtc152+ w4dtc153+ w4dtc154+ w4dtc155
replace cram12=1 if cram12==2
replace cram3=1 if cram3==3
gen teclear= w4s3243+ w4s3244+ w4s3245
gen teachcare= w4s3282+ w4s3283+ w4s3284+ w4s3285
gen discussenroll= w3s3281+ w3s3282+ w3s3283
label variable discussenroll "家人談升學就業"
drop w3p216
gen classinter= w4s3262+ w4s3263+ w4s3264+ w4s3265
label define w3p110 0 "沒有" 1 "有" 97 "不合理值" 99 "未填答", replace
label define w4p110 0 "沒有" 1 "有" 97 "不合理值" 99 "未填答", replace
replace  w3p110 =0 if w3p110 ==1
replace  w3p110 =1 if w3p110 ==2
replace  w4p110 =0 if w4p110 ==1
replace  w4p110 =1 if w4p110 ==2
gen familyhealthcare= w3p110+ w4p110
label define w3mtc30 3 "一定有" 2 "有時" 1 "偶爾" 0 "從不+沒出作業" 97 "不合理值" 99 "未填答", replace
replace w3mtc30=0 if w3mtc30==5
replace w3mtc30=0 if w3mtc30==4
replace w3mtc30=6 if w3mtc30==3
replace w3mtc30=3 if w3mtc30==1
replace w3mtc30=1 if w3mtc30==6
label define w3mtc31 3 "一定有" 2 "有時" 1 "偶爾" 0 "從不+沒出作業" 97 "不合理值" 99 "未填答", replace
replace w3mtc31=0 if w3mtc31==5
replace w3mtc31=0 if w3mtc31==4
replace w3mtc31=6 if w3mtc31==3
replace w3mtc31=3 if w3mtc31==1
replace w3mtc31=1 if w3mtc31==6
label define w3mtc32 3 "一定有" 2 "有時" 1 "偶爾" 0 "從不+沒出作業" 97 "不合理值" 99 "未填答", replace
replace w3mtc32=0 if w3mtc32==5
replace w3mtc32=0 if w3mtc32==4
replace w3mtc32=6 if w3mtc32==3
replace w3mtc32=3 if w3mtc32==1
replace w3mtc32=1 if w3mtc32==6
label define w3mtc33 3 "一定有" 2 "有時" 1 "偶爾" 0 "從不+沒出作業" 97 "不合理值" 99 "未填答", replace
replace w3mtc33=0 if w3mtc33==5
replace w3mtc33=0 if w3mtc33==4
replace w3mtc33=6 if w3mtc33==3
replace w3mtc33=3 if w3mtc33==1
replace w3mtc33=1 if w3mtc33==6
label define w3mtc34 3 "一定有" 2 "有時" 1 "偶爾" 0 "從不+沒出作業" 97 "不合理值" 99 "未填答", replace
replace w3mtc34=0 if w3mtc34==5
replace w3mtc34=0 if w3mtc34==4
replace w3mtc34=6 if w3mtc34==3
replace w3mtc34=3 if w3mtc34==1
replace w3mtc34=1 if w3mtc34==6
label define w3mtc35 3 "一定有" 2 "有時" 1 "偶爾" 0 "從不+沒出作業" 97 "不合理值" 99 "未填答", replace
replace w3mtc35=0 if w3mtc35==5
replace w3mtc35=0 if w3mtc35==4
replace w3mtc35=6 if w3mtc35==3
replace w3mtc35=3 if w3mtc35==1
replace w3mtc35=1 if w3mtc35==6
label define w3ctc30 3 "一定有" 2 "有時" 1 "偶爾" 0 "從不+沒出作業" 97 "不合理值" 99 "未填答", replace
replace w3ctc30=0 if w3ctc30==5
replace w3ctc30=0 if w3ctc30==4
replace w3ctc30=6 if w3ctc30==3
replace w3ctc30=3 if w3ctc30==1
replace w3ctc30=1 if w3ctc30==6
label define w3ctc31 3 "一定有" 2 "有時" 1 "偶爾" 0 "從不+沒出作業" 97 "不合理值" 99 "未填答", replace
replace w3ctc31=0 if w3ctc31==5
replace w3ctc31=0 if w3ctc31==4
replace w3ctc31=6 if w3ctc31==3
replace w3ctc31=3 if w3ctc31==1
replace w3ctc31=1 if w3ctc31==6
label define w3ctc32 3 "一定有" 2 "有時" 1 "偶爾" 0 "從不+沒出作業" 97 "不合理值" 99 "未填答", replace
replace w3ctc32=0 if w3ctc32==5
replace w3ctc32=0 if w3ctc32==4
replace w3ctc32=6 if w3ctc32==3
replace w3ctc32=3 if w3ctc32==1
replace w3ctc32=1 if w3ctc32==6
label define w3ctc33 3 "一定有" 2 "有時" 1 "偶爾" 0 "從不+沒出作業" 97 "不合理值" 99 "未填答", replace
replace w3ctc33=0 if w3ctc33==5
replace w3ctc33=0 if w3ctc33==4
replace w3ctc33=6 if w3ctc33==3
replace w3ctc33=3 if w3ctc33==1
replace w3ctc33=1 if w3ctc33==6
label define w3ctc34 3 "一定有" 2 "有時" 1 "偶爾" 0 "從不+沒出作業" 97 "不合理值" 99 "未填答", replace
replace w3ctc34=0 if w3ctc34==5
replace w3ctc34=0 if w3ctc34==4
replace w3ctc34=6 if w3ctc34==3
replace w3ctc34=3 if w3ctc34==1
replace w3ctc34=1 if w3ctc34==6
label define w3ctc35 3 "一定有" 2 "有時" 1 "偶爾" 0 "從不+沒出作業" 97 "不合理值" 99 "未填答", replace
replace w3ctc35=0 if w3ctc35==5
replace w3ctc35=0 if w3ctc35==4
replace w3ctc35=6 if w3ctc35==3
replace w3ctc35=3 if w3ctc35==1
replace w3ctc35=1 if w3ctc35==6
label define w3etc30 3 "一定有" 2 "有時" 1 "偶爾" 0 "從不+沒出作業" 97 "不合理值" 99 "未填答", replace
replace w3etc30=0 if w3etc30==5
replace w3etc30=0 if w3etc30==4
replace w3etc30=6 if w3etc30==3
replace w3etc30=3 if w3etc30==1
replace w3etc30=1 if w3etc30==6
label define w3etc31 3 "一定有" 2 "有時" 1 "偶爾" 0 "從不+沒出作業" 97 "不合理值" 99 "未填答", replace
replace w3etc31=0 if w3etc31==5
replace w3etc31=0 if w3etc31==4
replace w3etc31=6 if w3etc31==3
replace w3etc31=3 if w3etc31==1
replace w3etc31=1 if w3etc31==6
label define w3etc32 3 "一定有" 2 "有時" 1 "偶爾" 0 "從不+沒出作業" 97 "不合理值" 99 "未填答", replace
replace w3etc32=0 if w3etc32==5
replace w3etc32=0 if w3etc32==4
replace w3etc32=6 if w3etc32==3
replace w3etc32=3 if w3etc32==1
replace w3etc32=1 if w3etc32==6
label define w3etc33 3 "一定有" 2 "有時" 1 "偶爾" 0 "從不+沒出作業" 97 "不合理值" 99 "未填答", replace
replace w3etc33=0 if w3etc33==5
replace w3etc33=0 if w3etc33==4
replace w3etc33=6 if w3etc33==3
replace w3etc33=3 if w3etc33==1
replace w3etc33=1 if w3etc33==6
label define w3etc34 3 "一定有" 2 "有時" 1 "偶爾" 0 "從不+沒出作業" 97 "不合理值" 99 "未填答", replace
replace w3etc34=0 if w3etc34==5
replace w3etc34=0 if w3etc34==4
replace w3etc34=6 if w3etc34==3
replace w3etc34=3 if w3etc34==1
replace w3etc34=1 if w3etc34==6
label define w3etc35 3 "一定有" 2 "有時" 1 "偶爾" 0 "從不+沒出作業" 97 "不合理值" 99 "未填答", replace
replace w3etc35=0 if w3etc35==5
replace w3etc35=0 if w3etc35==4
replace w3etc35=6 if w3etc35==3
replace w3etc35=3 if w3etc35==1
replace w3etc35=1 if w3etc35==6
gen cthm= w3ctc30+ w3ctc31+ w3ctc32+ w3ctc33+ w3ctc34+ w3ctc35
gen mahm= w3mtc30+ w3mtc31+ w3mtc32+ w3mtc33+ w3mtc34+ w3mtc35
gen enhm= w3etc30+ w3etc31+ w3etc32+ w3etc33+ w3etc34+ w3etc35
gen loan= w4p2333+w4p2334+w4p2335
label define w3p110 0 "沒有" 1 "有" 97 "不合理值" 99 "未填答", replace
label define w4p110 0 "沒有" 1 "有" 97 "不合理值" 99 "未填答", replace
label variable familyhealthcare "家人長期臥病"
label define w4s444 0 "從來沒有" 1 "偶爾有" 2 "有時有" 3 "經常有" 97 "不合理值" 99 "未填答", replace
replace w4s444=0 if w4s444==1
replace w4s444=1 if w4s444==2
replace w4s444=2 if w4s444==3
replace w4s444=3 if w4s444==4
label define w4s449 0 "從來沒有" 1 "偶爾有" 2 "有時有" 3 "經常有" 97 "不合理值" 99 "未填答", replace
replace w4s449=0 if w4s449==1
replace w4s449=1 if w4s449==2
replace w4s449=2 if w4s449==3
replace w4s449=3 if w4s449==4
label define w4s450 0 "從來沒有" 1 "偶爾有" 2 "有時有" 3 "經常有" 97 "不合理值" 99 "未填答", replace
replace w4s450=0 if w4s450==1
replace w4s450=1 if w4s450==2
replace w4s450=2 if w4s450==3
replace w4s450=3 if w4s450==4
label define w4s451 0 "從來沒有" 1 "偶爾有" 2 "有時有" 3 "經常有" 97 "不合理值" 99 "未填答", replace
replace w4s451=0 if w4s451==1
replace w4s451=1 if w4s451==2
replace w4s451=2 if w4s451==3
replace w4s451=3 if w4s451==4
label define w4s452 0 "從來沒有" 1 "偶爾有" 2 "有時有" 3 "經常有" 97 "不合理值" 99 "未填答", replace
replace w4s452=0 if w4s452==1
replace w4s452=1 if w4s452==2
replace w4s452=2 if w4s452==3
replace w4s452=3 if w4s452==4
label define w4s453 0 "從來沒有" 1 "偶爾有" 2 "有時有" 3 "經常有" 97 "不合理值" 99 "未填答", replace
replace w4s453=0 if w4s453==1
replace w4s453=1 if w4s453==2
replace w4s453=2 if w4s453==3
replace w4s453=3 if w4s453==4
label define w4s455 0 "從來沒有" 1 "偶爾有" 2 "有時有" 3 "經常有" 97 "不合理值" 99 "未填答", replace
replace w4s455=0 if w4s455==1
replace w4s455=1 if w4s455==2
replace w4s455=2 if w4s455==3
replace w4s455=3 if w4s455==4
label define w4s456 0 "從來沒有" 1 "偶爾有" 2 "有時有" 3 "經常有" 97 "不合理值" 99 "未填答", replace
replace w4s456=0 if w4s456==1
replace w4s456=1 if w4s456==2
replace w4s456=2 if w4s456==3
replace w4s456=3 if w4s456==4
label define w4s457 0 "從來沒有" 1 "偶爾有" 2 "有時有" 3 "經常有" 97 "不合理值" 99 "未填答", replace
replace w4s457=0 if w4s457==1
replace w4s457=1 if w4s457==2
replace w4s457=2 if w4s457==3
replace w4s457=3 if w4s457==4
label define w4s458 0 "從來沒有" 1 "偶爾有" 2 "有時有" 3 "經常有" 97 "不合理值" 99 "未填答", replace
replace w4s458=0 if w4s458==1
replace w4s458=1 if w4s458==2
replace w4s458=2 if w4s458==3
replace w4s458=3 if w4s458==4
label define w4s459 0 "從來沒有" 1 "偶爾有" 2 "有時有" 3 "經常有" 97 "不合理值" 99 "未填答", replace
replace w4s459=0 if w4s459==1
replace w4s459=1 if w4s459==2
replace w4s459=2 if w4s459==3
replace w4s459=3 if w4s459==4
label define w4s409 0 "沒想過" 1 "高中" 2 "大學或科技大學" 3 "碩士"  4 "博士" 97 "不合理值" 99 "未填答", replace
replace w4s409=2 if w4s409==3
replace w4s409=3 if w4s409==4
replace w4s409=4 if w4s409==5
replace w4s409=0 if w4s409==6
replace w4s335=0.2 if w4s335==1
replace w4s335=0.5 if w4s335==2
replace w4s335=1 if w4s335==3
replace w4s335=2.5 if w4s335==4
replace w4s335=4.5 if w4s335==5
replace w4s335=6.5 if w4s335==6
label define w4dtc13 0 "都沒有" 1 "1次" 2 "2次" 3 "3次" 4 "4次" 5 "5次以上" 97 "不合理值" 99 "未填答", replace
replace  w4dtc13 =0 if w4dtc13==1
replace  w4dtc13 =1 if w4dtc13==2
replace  w4dtc13 =2 if w4dtc13==3
replace  w4dtc13 =3 if w4dtc13==4
replace  w4dtc13 =4 if w4dtc13==5
replace  w4dtc13 =5 if w4dtc13==6
replace w4s314=0 if w4s314==1
replace w4s314=1.5 if w4s314==2
replace w4s314=3.5 if w4s314==3
replace w4s314=5.5 if w4s314==4
replace w4s314=7 if w4s314==5
replace w4s315=0 if w4s315==1
replace w4s315=1.5 if w4s315==2
replace w4s315=3.5 if w4s315==3
replace w4s315=5.5 if w4s315==4
replace w4s315=7 if w4s315==5
replace w4s319=0 if w4s319==1
replace w4s319=1.5 if w4s319==2
replace w4s319=3.5 if w4s319==3
replace w4s319=5.5 if w4s319==4
replace w4s319=7 if w4s319==5
replace w3p602=2.5 if w3p602==2
replace w3p602=9 if w3p602==3
replace w3p602=7.5 if w3p602==4
replace w3p602=4 if w3p602==9
replace w3p602=15 if w3p602==5
replace w3p602=30 if w3p602==6
replace enhm=. if enhm==594
replace enhm=18 if enhm==117
replace enhm=16 if enhm==113
replace enhm=15 if enhm==112
replace scteamatt=. if scteamatt==297
replace outclubatt=0 if outclubatt==297
replace outclubatt=1 if outclubatt==298
replace outclubatt=2 if outclubatt==299
replace outclubatt=3 if outclubatt==300
replace outclubatt=. if outclubatt==594
replace freecram=. if freecram==297
replace ctcfor3=. if ctcfor3==485
replace mtcfor3=. if mtcfor3==485
replace etcfor3=. if etcfor3==485
replace loan=. if loan==297
replace teclear=. if teclear==297
replace w3s3315=. if w3s3315==99
replace teachcare=. if teachcare==396
 replace classinter=. if classinter==396
 replace  w3s3284=. if  w3s3284==99
replace  w3s3285=. if  w3s3285==99
replace w4s2075=. if w4s2075==99
replace w4s2085=. if w4s2085==99
replace w4s2095=. if w4s2095==99
replace w4s2105=. if w4s2105==99
replace w4s2115=. if w4s2115==99
replace w4s2065=. if w4s2065==99
replace familyhealthcare=. if familyhealthcare==97
replace familyhealthcare=0 if familyhealthcare==99
replace familyhealthcare=1 if familyhealthcare==100
replace discussenroll=. if discussenroll==297
label define w4p202 3 "非常需要" 2 "需要" 1 "不需要" 0 "非常不需要" 97 "不合理值" 99 "未填答", replace
replace w4p202=5 if w4p202==1
replace w4p202=1 if w4p202==3
replace w4p202=3 if w4p202==5
replace w4p202=0 if w4p202==4
label define w4p412 3 "非常需要" 2 "需要" 1 "不需要" 0 "非常不需要" 97 "不合理值" 99 "未填答", replace
replace w4p412=5 if w4p412==1
replace w4p412=1 if w4p412==3
replace w4p412=3 if w4p412==5
replace w4p412=0 if w4p412==4
replace w4p202=. if w4p202==99
replace w4p202=. if w4p202==97
label define w4s110 3 "非常有幫助" 2 "有幫助" 1 "沒有幫助" 0 "非常沒有幫助" 97 "不合理值" 99 "未填答", replace
replace w4s110=0 if w4s110==4
replace w4s110=5 if w4s110==3
replace w4s110=3 if w4s110==1
replace w4s110=1 if w4s110==5
label define w4s111 3 "非常有幫助" 2 "有幫助" 1 "沒有幫助" 0 "非常沒有幫助" 97 "不合理值" 99 "未填答", replace
replace w4s111=0 if w4s111==4
replace w4s111=5 if w4s111==3
replace w4s111=3 if w4s111==1
replace w4s111=1 if w4s111==5
gen crammathhelp= w4s110+ w4s111
replace crammathhelp=. if crammathhelp==198
replace crammathhelp=. if crammathhelp==97
replace crammathhelp=1 if crammathhelp==100
replace crammathhelp=2 if crammathhelp==101
replace crammathhelp=3 if crammathhelp==102
label define w4p318 3 "非常有幫助" 2 "有幫助" 1 "沒有幫助" 0 "非常沒有幫助" 97 "不合理值" 99 "未填答", replace
replace w4p318=0 if w4p318==4
replace w4p318=5 if w4p318==3
replace w4p318=3 if w4p318==1
replace w4p318=1 if w4p318==5
label define w4p319 3 "非常有幫助" 2 "有幫助" 1 "沒有幫助" 0 "非常沒有幫助" 97 "不合理值" 99 "未填答", replace
replace w4p319=0 if w4p319==4
replace w4p319=5 if w4p319==3
replace w4p319=3 if w4p319==1
replace w4p319=1 if w4p319==5
gen parentmathcramhelp= w4p318+ w4p319
replace parentmathcramhelp=. if parentmathcramhelp==198
replace parentmathcramhelp=0 if parentmathcramhelp==99
replace parentmathcramhelp=2 if parentmathcramhelp==101
replace parentmathcramhelp=3 if parentmathcramhelp==102
label define w3t311 0 "幾乎不會" 1 "部分老師會" 2 "至少一半老師會" 3 "幾乎每個老師都會" 0 "不知道" 97 "不合理值" 99 "未填答", replace
replace w3t311=0 if w3t311 ==4| w3t311 ==5
replace w3t311=4 if w3t311 ==3
replace w3t311=3 if w3t311 ==1
replace w3t311=1 if w3t311 ==4
label define w3t316 0 "沒有" 1 "偶爾" 2 "有時" 3 "經常" 97 "不合理值" 99 "未填答", replace
replace w3t316=0 if w3t316==1
replace w3t316=1 if w3t316==2
replace w3t316=2 if w3t316==3
replace w3t316=3 if w3t316==4
label define w3t317 0 "沒有" 1 "偶爾" 2 "有時" 3 "經常" 97 "不合理值" 99 "未填答", replace
replace w3t317=0 if w3t317==1
replace w3t317=1 if w3t317==2
replace w3t317=2 if w3t317==3
replace w3t317=3 if w3t317==4
label define w3ctc16 3 "經常" 2 "有時" 1 "偶爾" 0 "從不" 97 "不合理值" 99 "未填答", replace
replace w3ctc16=5 if w3ctc16==1
replace w3ctc16=0 if w3ctc16==4
replace w3ctc16=1 if w3ctc16==3
replace w3ctc16=3 if w3ctc16==5
label define w3mtc16 3 "經常" 2 "有時" 1 "偶爾" 0 "從不" 97 "不合理值" 99 "未填答", replace
replace w3mtc16=5 if w3mtc16==1
replace w3mtc16=0 if w3mtc16==4
replace w3mtc16=1 if w3mtc16==3
replace w3mtc16=3 if w3mtc16==5
label define w3etc16 3 "經常" 2 "有時" 1 "偶爾" 0 "從不" 97 "不合理值" 99 "未填答", replace
replace w3etc16=5 if w3etc16==1
replace w3etc16=0 if w3etc16==4
replace w3etc16=1 if w3etc16==3
replace w3etc16=3 if w3etc16==5
label drop w3ctc20
replace w3ctc20=0 if w3ctc20==1
replace w3ctc20=0.5 if w3ctc20==2
replace w3ctc20=1 if w3ctc20==3
replace w3ctc20=2 if w3ctc20==4
replace w3ctc20=3 if w3ctc20==5
replace w3ctc20=4 if w3ctc20==6
label drop w3ctc21
replace w3ctc21=0 if w3ctc21==1
replace w3ctc21=0.5 if w3ctc21==2
replace w3ctc21=1 if w3ctc21==3
replace w3ctc21=2 if w3ctc21==4
replace w3ctc21=3 if w3ctc21==5
replace w3ctc21=4 if w3ctc21==6
label drop w3mtc20
replace w3mtc20=0 if w3mtc20==1
replace w3mtc20=0.5 if w3mtc20==2
replace w3mtc20=1 if w3mtc20==3
replace w3mtc20=2 if w3mtc20==4
replace w3mtc20=3 if w3mtc20==5
replace w3mtc20=4 if w3mtc20==6
label drop w3mtc21
replace w3mtc21=0 if w3mtc21==1
replace w3mtc21=0.5 if w3mtc21==2
replace w3mtc21=1 if w3mtc21==3
replace w3mtc21=2 if w3mtc21==4
replace w3mtc21=3 if w3mtc21==5
replace w3mtc21=4 if w3mtc21==6
label drop w3etc20
replace w3etc20=0 if w3etc20==1
replace w3etc20=0.5 if w3etc20==2
replace w3etc20=1 if w3etc20==3
replace w3etc20=2 if w3etc20==4
replace w3etc20=3 if w3etc20==5
replace w3etc20=4 if w3etc20==6
label drop w3etc21
replace w3etc21=0 if w3etc21==1
replace w3etc21=0.5 if w3etc21==2
replace w3etc21=1 if w3etc21==3
replace w3etc21=2 if w3etc21==4
replace w3etc21=3 if w3etc21==5
replace w3etc21=4 if w3etc21==6
label define w3ctc05 4 "特別好" 3 "比較好" 2 "差不多" 1 "比較差" 0 "特別差" 97 "不合理值" 99 "未填答", replace
replace w3ctc05=7 if w3ctc05==1
replace w3ctc05=8 if w3ctc05==2
replace w3ctc05=2 if w3ctc05==3
replace w3ctc05=1 if w3ctc05==4
replace w3ctc05=0 if w3ctc05==5
replace w3ctc05=0 if w3ctc05==6
replace w3ctc05=3 if w3ctc05==8
replace w3ctc05=4 if w3ctc05==7
label define w3etc05 4 "特別好" 3 "比較好" 2 "差不多" 1 "比較差" 0 "特別差" 97 "不合理值" 99 "未填答", replace
replace w3etc05=7 if w3etc05==1
replace w3etc05=8 if w3etc05==2
replace w3etc05=2 if w3etc05==3
replace w3etc05=1 if w3etc05==4
replace w3etc05=0 if w3etc05==5
replace w3etc05=0 if w3etc05==6
replace w3etc05=3 if w3etc05==8
replace w3etc05=4 if w3etc05==7
label define w3mtc05 4 "特別好" 3 "比較好" 2 "差不多" 1 "比較差" 0 "特別差" 97 "不合理值" 99 "未填答", replace
replace w3mtc05=7 if w3mtc05==1
replace w3mtc05=8 if w3mtc05==2
replace w3mtc05=2 if w3mtc05==3
replace w3mtc05=1 if w3mtc05==4
replace w3mtc05=0 if w3mtc05==5
replace w3mtc05=0 if w3mtc05==6
replace w3mtc05=3 if w3mtc05==8
replace w3mtc05=4 if w3mtc05==7
label define w4ctc07 4 "特別好" 3 "比較好" 2 "差不多" 1 "比較差" 0 "特別差" 97 "不合理值" 99 "未填答", replace
replace w4ctc07=7 if w4ctc07==1
replace w4ctc07=8 if w4ctc07==2
replace w4ctc07=2 if w4ctc07==3
replace w4ctc07=1 if w4ctc07==4
replace w4ctc07=0 if w4ctc07==5
replace w4ctc07=0 if w4ctc07==6
replace w4ctc07=3 if w4ctc07==8
replace w4ctc07=4 if w4ctc07==7
label define w4etc07 4 "特別好" 3 "比較好" 2 "差不多" 1 "比較差" 0 "特別差" 97 "不合理值" 99 "未填答", replace
replace w4etc07=7 if w4etc07==1
replace w4etc07=8 if w4etc07==2
replace w4etc07=2 if w4etc07==3
replace w4etc07=1 if w4etc07==4
replace w4etc07=0 if w4etc07==5
replace w4etc07=0 if w4etc07==6
replace w4etc07=3 if w4etc07==8
replace w4etc07=4 if w4etc07==7
label define w4mtc07 4 "特別好" 3 "比較好" 2 "差不多" 1 "比較差" 0 "特別差" 97 "不合理值" 99 "未填答", replace
replace w4mtc07=7 if w4mtc07==1
replace w4mtc07=8 if w4mtc07==2
replace w4mtc07=2 if w4mtc07==3
replace w4mtc07=1 if w4mtc07==4
replace w4mtc07=0 if w4mtc07==5
replace w4mtc07=0 if w4mtc07==6
replace w4mtc07=3 if w4mtc07==8
replace w4mtc07=4 if w4mtc07==7
label define w3dtc03 4 "特別好" 3 "比較好" 2 "差不多" 1 "比較差" 0 "特別差" 97 "不合理值" 99 "未填答", replace
replace w3dtc03=7 if w3dtc03==1
replace w3dtc03=8 if w3dtc03==2
replace w3dtc03=2 if w3dtc03==3
replace w3dtc03=1 if w3dtc03==4
replace w3dtc03=0 if w3dtc03==5
replace w3dtc03=0 if w3dtc03==6
replace w3dtc03=3 if w3dtc03==8
replace w3dtc03=4 if w3dtc03==7
label define w4dtc03 4 "特別好" 3 "比較好" 2 "差不多" 1 "比較差" 0 "特別差" 97 "不合理值" 99 "未填答", replace
replace w4dtc03=7 if w4dtc03==1
replace w4dtc03=8 if w4dtc03==2
replace w4dtc03=2 if w4dtc03==3
replace w4dtc03=1 if w4dtc03==4
replace w4dtc03=0 if w4dtc03==5
replace w4dtc03=0 if w4dtc03==6
replace w4dtc03=3 if w4dtc03==8
replace w4dtc03=4 if w4dtc03==7
label define w3ctc06 4 "要求達到前一,二名" 3 "平均水準以上" 2 "大約平均水準" 1 "不要墊底就好" 0 "沒有要求" 0 "無法比較或其他" 97 "不合理值" 99 "未填答", replace
replace w3ctc06=7 if w3ctc06==1
replace w3ctc06=8 if w3ctc06==2
replace w3ctc06=2 if w3ctc06==3
replace w3ctc06=1 if w3ctc06==4
replace w3ctc06=0 if w3ctc06==5
replace w3ctc06=0 if w3ctc06==6
replace w3ctc06=4 if w3ctc06==7
replace w3ctc06=3 if w3ctc06==8
label define w3mtc06 4 "要求達到前一,二名" 3 "平均水準以上" 2 "大約平均水準" 1 "不要墊底就好" 0 "沒有要求" 0 "無法比較或其他" 97 "不合理值" 99 "未填答", replace
replace w3mtc06=7 if w3mtc06==1
replace w3mtc06=8 if w3mtc06==2
replace w3mtc06=2 if w3mtc06==3
replace w3mtc06=1 if w3mtc06==4
replace w3mtc06=0 if w3mtc06==5
replace w3mtc06=0 if w3mtc06==6
replace w3mtc06=4 if w3mtc06==7
replace w3mtc06=3 if w3mtc06==8
label define w3etc06 4 "要求達到前一,二名" 3 "平均水準以上" 2 "大約平均水準" 1 "不要墊底就好" 0 "沒有要求" 0 "無法比較或其他" 97 "不合理值" 99 "未填答", replace
replace w3etc06=7 if w3etc06==1
replace w3etc06=8 if w3etc06==2
replace w3etc06=2 if w3etc06==3
replace w3etc06=1 if w3etc06==4
replace w3etc06=0 if w3etc06==5
replace w3etc06=0 if w3etc06==6
replace w3etc06=4 if w3etc06==7
replace w3etc06=3 if w3etc06==8
label define w4ctc09 4 "要求達到前一,二名" 3 "平均水準以上" 2 "大約平均水準" 1 "不要墊底就好" 0 "沒有要求" 0 "無法比較或其他" 97 "不合理值" 99 "未填答", replace
replace w4ctc09=7 if w4ctc09==1
replace w4ctc09=8 if w4ctc09==2
replace w4ctc09=2 if w4ctc09==3
replace w4ctc09=1 if w4ctc09==4
replace w4ctc09=0 if w4ctc09==5
replace w4ctc09=0 if w4ctc09==6
replace w4ctc09=4 if w4ctc09==7
replace w4ctc09=3 if w4ctc09==8
label define w4mtc09 4 "要求達到前一,二名" 3 "平均水準以上" 2 "大約平均水準" 1 "不要墊底就好" 0 "沒有要求" 0 "無法比較或其他" 97 "不合理值" 99 "未填答", replace
replace w4mtc09=7 if w4mtc09==1
replace w4mtc09=8 if w4mtc09==2
replace w4mtc09=2 if w4mtc09==3
replace w4mtc09=1 if w4mtc09==4
replace w4mtc09=0 if w4mtc09==5
replace w4mtc09=0 if w4mtc09==6
replace w4mtc09=4 if w4mtc09==7
replace w4mtc09=3 if w4mtc09==8
label define w4etc09 4 "要求達到前一,二名" 3 "平均水準以上" 2 "大約平均水準" 1 "不要墊底就好" 0 "沒有要求" 0 "無法比較或其他" 97 "不合理值" 99 "未填答", replace
replace w4etc09=7 if w4etc09==1
replace w4etc09=8 if w4etc09==2
replace w4etc09=2 if w4etc09==3
replace w4etc09=1 if w4etc09==4
replace w4etc09=0 if w4etc09==5
replace w4etc09=0 if w4etc09==6
replace w4etc09=4 if w4etc09==7
replace w4etc09=3 if w4etc09==8
label define w4p207 3"經常會" 2"有時會" 1"偶爾會" 0"幾乎不會",replace
replace w4p207=5 if w4p207==1
replace w4p207=1 if w4p207==3
replace w4p207=0 if w4p207==4
replace w4p207=3 if w4p207==5
label define w4p208 3"經常會" 2"有時會" 1"偶爾會" 0"幾乎不會",replace
replace w4p208=5 if w4p208==1
replace w4p208=1 if w4p208==3
replace w4p208=0 if w4p208==4
replace w4p208=3 if w4p208==5
label define w4p209 3"經常會" 2"有時會" 1"偶爾會" 0"幾乎不會",replace
replace w4p209=5 if w4p209==1
replace w4p209=1 if w4p209==3
replace w4p209=0 if w4p209==4
replace w4p209=3 if w4p209==5
label define w3dtc09 3"經常會" 2"有時會" 1"偶爾會" 0"幾乎不會",replace
replace w3dtc09=5 if w3dtc09==1
replace w3dtc09=1 if w3dtc09==3
replace w3dtc09=0 if w3dtc09==4
replace w3dtc09=3 if w3dtc09==5
label define w3dtc13 3"經常會" 2"有時會" 1"偶爾會" 0"幾乎不會",replace
replace w3dtc13=5 if w3dtc13==1
replace w3dtc13=1 if w3dtc13==3
replace w3dtc13=0 if w3dtc13==4
replace w3dtc13=3 if w3dtc13==5
label define w3s313 3"經常會" 2"有時會" 1"偶爾會" 0"幾乎不會",replace
replace w3s313=6 if w3s313==1
replace w3s313=1 if w3s313==3
replace w3s313=0 if w3s313==4
replace w3s313=0 if w3s313==5
replace w3s313=3 if w3s313==6
label define w3s315 3"經常會" 2"有時會" 1"偶爾會" 0"幾乎不會",replace
replace w3s315=6 if w3s315==1
replace w3s315=1 if w3s315==3
replace w3s315=0 if w3s315==4
replace w3s315=0 if w3s315==5
replace w3s315=3 if w3s315==6
label define w3s320 3"經常會" 2"有時會" 1"偶爾會" 0"幾乎不會",replace
replace w3s320=6 if w3s320==1
replace w3s320=1 if w3s320==3
replace w3s320=0 if w3s320==4
replace w3s320=0 if w3s320==5
replace w3s320=3 if w3s320==6
label define w3s322 3"經常會" 2"有時會" 1"偶爾會" 0"幾乎不會",replace
replace w3s322=6 if w3s322==1
replace w3s322=1 if w3s322==3
replace w3s322=0 if w3s322==4
replace w3s322=0 if w3s322==5
replace w3s322=3 if w3s322==6
label define w4p226 3"經常會" 2"有時會" 1"偶爾會" 0"幾乎不會",replace
replace w4p226=6 if w4p226==1
replace w4p226=1 if w4p226==3
replace w4p226=0 if w4p226==4
replace w4p226=0 if w4p226==5
replace w4p226=3 if w4p226==6
label define w4ctc24 3"經常會" 2"有時會" 1"偶爾會" 0"幾乎不會",replace
replace w4ctc24=6 if w4ctc24==1
replace w4ctc24=1 if w4ctc24==3
replace w4ctc24=0 if w4ctc24==4
replace w4ctc24=0 if w4ctc24==5
replace w4ctc24=3 if w4ctc24==6
label define w4mtc24 3"經常會" 2"有時會" 1"偶爾會" 0"幾乎不會",replace
replace w4mtc24=6 if w4mtc24==1
replace w4mtc24=1 if w4mtc24==3
replace w4mtc24=0 if w4mtc24==4
replace w4mtc24=0 if w4mtc24==5
replace w4mtc24=3 if w4mtc24==6
label define w4etc24 3"經常會" 2"有時會" 1"偶爾會" 0"幾乎不會",replace
replace w4etc24=6 if w4etc24==1
replace w4etc24=1 if w4etc24==3
replace w4etc24=0 if w4etc24==4
replace w4etc24=0 if w4etc24==5
replace w4etc24=3 if w4etc24==6
label define w4t216 3"經常會" 2"有時會" 1"偶爾會" 0"幾乎不會",replace
replace w4t216=6 if w4t216==1
replace w4t216=1 if w4t216==3
replace w4t216=0 if w4t216==4
replace w4t216=0 if w4t216==5
replace w4t216=3 if w4t216==6
label define w4t217 3"經常會" 2"有時會" 1"偶爾會" 0"幾乎不會",replace
replace w4t217=6 if w4t217==1
replace w4t217=1 if w4t217==3
replace w4t217=0 if w4t217==4
replace w4t217=0 if w4t217==5
replace w4t217=3 if w4t217==6
label drop w4ctc28
replace w4ctc28=0 if w4ctc28==1
replace w4ctc28=0.5 if w4ctc28==2
replace w4ctc28=1 if w4ctc28==3
replace w4ctc28=2 if w4ctc28==4
replace w4ctc28=3 if w4ctc28==5
replace w4ctc28=4 if w4ctc28==6
label drop w4etc28
replace w4etc28=0 if w4etc28==1
replace w4etc28=0.5 if w4etc28==2
replace w4etc28=1 if w4etc28==3
replace w4etc28=2 if w4etc28==4
replace w4etc28=3 if w4etc28==5
replace w4etc28=4 if w4etc28==6
label drop w4mtc28
replace w4mtc28=0 if w4mtc28==1
replace w4mtc28=0.5 if w4mtc28==2
replace w4mtc28=1 if w4mtc28==3
replace w4mtc28=2 if w4mtc28==4
replace w4mtc28=3 if w4mtc28==5
replace w4mtc28=4 if w4mtc28==6
label drop w4mtc29
replace w4mtc29=0 if w4mtc29==1
replace w4mtc29=0.5 if w4mtc29==2
replace w4mtc29=1 if w4mtc29==3
replace w4mtc29=2 if w4mtc29==4
replace w4mtc29=3 if w4mtc29==5
replace w4mtc29=4 if w4mtc29==6
label drop w4ctc29
replace w4ctc29=0 if w4ctc29==1
replace w4ctc29=0.5 if w4ctc29==2
replace w4ctc29=1 if w4ctc29==3
replace w4ctc29=2 if w4ctc29==4
replace w4ctc29=3 if w4ctc29==5
replace w4ctc29=4 if w4ctc29==6
label drop w4etc29
replace w4etc29=0 if w4etc29==1
replace w4etc29=0.5 if w4etc29==2
replace w4etc29=1 if w4etc29==3
replace w4etc29=2 if w4etc29==4
replace w4etc29=3 if w4etc29==5
replace w4etc29=4 if w4etc29==6
label drop w3s121
replace w3s121=0 if w3s121==4
replace w3s121=5 if w3s121==3
replace w3s121=3 if w3s121==2
label drop w3p209 w3p212
replace w3p209=0 if w3p209==1|w3p209==5
replace w3p209=1 if w3p209==2
replace w3p209=2 if w3p209==3
replace w3p209=3 if w3p209==4
replace w3p212=0 if w3p212==1|w3p212==5
replace w3p212=1 if w3p212==2
replace w3p212=2 if w3p212==3
replace w3p212=3 if w3p212==4
label drop w3tcs2 w3tcs3 w3tcs4 w3tes2 w3tes3 w3tes4 w3tms2 w3tms3 w3tms4
replace w3tcs2=0 if w3tcs2==4|w3tcs2==5
replace w3tcs2=6 if w3tcs2==1
replace w3tcs2=1 if w3tcs2==3
replace w3tcs2=3 if w3tcs2==6
replace w3tcs3=0 if w3tcs3==4|w3tcs3==5
replace w3tcs3=6 if w3tcs3==1
replace w3tcs3=1 if w3tcs3==3
replace w3tcs3=3 if w3tcs3==6
replace w3tcs4=0 if w3tcs4==4|w3tcs4==5
replace w3tcs4=6 if w3tcs4==1
replace w3tcs4=1 if w3tcs4==3
replace w3tcs4=3 if w3tcs4==6
replace w3tes2=0 if w3tes2==4|w3tes2==5
replace w3tes2=6 if w3tes2==1
replace w3tes2=1 if w3tes2==3
replace w3tes2=3 if w3tes2==6
replace w3tes3=0 if w3tes3==4|w3tes3==5
replace w3tes3=6 if w3tes3==1
replace w3tes3=1 if w3tes3==3
replace w3tes3=3 if w3tes3==6
replace w3tes4=0 if w3tes4==4|w3tes4==5
replace w3tes4=6 if w3tes4==1
replace w3tes4=1 if w3tes4==3
replace w3tes4=3 if w3tes4==6
replace w3tms2=0 if w3tms2==4|w3tms2==5
replace w3tms2=6 if w3tms2==1
replace w3tms2=1 if w3tms2==3
replace w3tms2=3 if w3tms2==6
replace w3tms3=0 if w3tms3==4|w3tms3==5
replace w3tms3=6 if w3tms3==1
replace w3tms3=1 if w3tms3==3
replace w3tms3=3 if w3tms3==6
replace w3tms4=0 if w3tms4==4|w3tms4==5
replace w3tms4=6 if w3tms4==1
replace w3tms4=1 if w3tms4==3
replace w3tms4=3 if w3tms4==6
replace w3s104=0 if  w3s104==3|w3s104==4|w3s104==5|w3s104==6
replace w3s104=1 if  w3s104==1|w3s104==2
label drop w3td07 w3td08 w4td03 w4td05
replace w3td07=0 if w3td07==5|w3td07==6
replace w3td07=7 if w3td07==4
replace w3td07=8 if w3td07==3
replace w3td07=3 if w3td07==2
replace w3td07=4 if w3td07==1
replace w3td07=1 if w3td07==7
replace w3td07=2 if w3td07==8
replace w3td08=0 if w3td08==5|w3td08==6
replace w3td08=7 if w3td08==4
replace w3td08=8 if w3td08==3
replace w3td08=3 if w3td08==2
replace w3td08=4 if w3td08==1
replace w3td08=1 if w3td08==7
replace w3td08=2 if w3td08==8
replace w4td03=0 if w4td03==5|w4td03==6
replace w4td03=7 if w4td03==4
replace w4td03=8 if w4td03==3
replace w4td03=3 if w4td03==2
replace w4td03=4 if w4td03==1
replace w4td03=1 if w4td03==7
replace w4td03=2 if w4td03==8
replace w4td05=0 if w4td05==5|w4td05==6
replace w4td05=7 if w4td05==4
replace w4td05=8 if w4td05==3
replace w4td05=3 if w4td05==2
replace w4td05=4 if w4td05==1
replace w4td05=1 if w4td05==7
replace w4td05=2 if w4td05==8
label drop w4p413 w4p229
replace w4p229=0 if w4p229==5|w4p229==4
replace w4p229=6 if w4p229==1
replace w4p229=1 if w4p229==3
replace w4p229=3 if w4p229==6
replace w4p413=0 if w4p413==5|w4p413==4
replace w4p413=6 if w4p413==1
replace w4p413=1 if w4p413==3
replace w4p413=3 if w4p413==6
label drop w3dtc14
replace w3dtc14=0 if w3dtc14==4
replace w3dtc14=6 if w3dtc14==1
replace w3dtc14=1 if w3dtc14==3
replace w3dtc14=3 if w3dtc14==6
label drop w3dtc08 w4dtc08
replace w3dtc08=0 if w3dtc08==4
replace w3dtc08=6 if w3dtc08==1
replace w3dtc08=1 if w3dtc08==3
replace w3dtc08=3 if w3dtc08==6
replace w4dtc08=0 if w4dtc08==4
replace w4dtc08=6 if w4dtc08==1
replace w4dtc08=1 if w4dtc08==3
replace w4dtc08=3 if w4dtc08==6
label drop w4p225 w4td06
replace w4p225=0 if w4p225==4|w4p225==5
replace w4p225=6 if w4p225==1
replace w4p225=1 if w4p225==3
replace w4p225=3 if w4p225==6
replace w4td06=0 if w4td06==4|w4td06==5
replace w4td06=6 if w4td06==1
replace w4td06=1 if w4td06==3
replace w4td06=3 if w4td06==6
label drop w4td07
replace w4td07=0 if w4td07==3|w4td07==2
replace w3p201=0 if w3p201==1|w3p201==3
replace w3p201=1 if w3p201==2
replace w4p219=0 if w4p219==1
replace w4p219=1 if w4p219==2
replace w4p219=2 if w4p219==3
replace w4p219=3 if w4p219==4
replace w4p219=4 if w4p219==5
replace w4p219=5 if w4p219==6
rename w4p219 commuschol
replace w3s460=11 if w3s460==2
replace w3s460=12 if w3s460==3
replace w3s460=8 if w3s460==4
replace w3s460=10 if w3s460==5
replace w3s460=3 if w3s460==11
replace w3s460=5 if w3s460==12
replace w3s460=0 if w3s460==6
label drop w3s460
replace w4s106=0 if w4s106==6
replace w4s106=6 if w4s106==2
replace w4s106=2 if w4s106==1
replace w4s106=10 if w4s106==3
replace w4s106=14 if w4s106==4
replace w4s106=18 if w4s106==5
replace w3s126=0 if w3s126==6
replace w3s126=6 if w3s126==2
replace w3s126=2 if w3s126==1
replace w3s126=10 if w3s126==3
replace w3s126=14 if w3s126==4
replace w3s126=18 if w3s126==5
label drop w4s106 w3s126
replace w3s106=0.5 if w3s106==1
replace w3s106=1.5 if w3s106==2
replace w3s106=2.5 if w3s106==3
replace w3s106=3.5 if w3s106==4
replace w3s106=5 if w3s106==5
replace w3s106=6 if w3s106==6
label drop w3s106
replace w4s106=. if w4s106==97|w4s106==99
replace w3s126=. if w3s126==97|w3s126==99
replace w4s106=w3s126 if w4s106==.
replace w3s126=w4s106 if w3s126==.
gen careclasstime= (w3s126+w4s106)/2
replace w3tcs2=. if w3tcs2==97|w3tcs2==99
replace w3tcs3=. if w3tcs3==97|w3tcs3==99
replace w3tcs4=. if w3tcs4==97|w3tcs4==99
replace w3tes2=. if w3tes2==97|w3tes2==99
replace w3tes3=. if w3tes3==97|w3tes3==99
replace w3tes4=. if w3tes4==97|w3tes4==99
replace w3tms2=. if w3tms2==97|w3tms2==99
replace w3tms3=. if w3tms3==97|w3tms3==99
replace w3tms4=. if w3tms4==97|w3tms4==99
replace w3tcs2=(w3tes2+w3tms2)/2 if w3tcs2==.
replace w3tcs3=(w3tes3+w3tms3)/2 if w3tcs3==.
replace w3tcs4=(w3tes4+w3tms4)/2 if w3tcs4==.
replace w3tes2=(w3tcs2+w3tms2)/2 if w3tes2==.
replace w3tes3=(w3tcs3+w3tms3)/2 if w3tes3==.
replace w3tes4=(w3tcs4+w3tms4)/2 if w3tes4==.
replace w3tms2=(w3tcs2+w3tes2)/2 if w3tms2==.
replace w3tms3=(w3tcs3+w3tes3)/2 if w3tms3==.
replace w3tms4=(w3tcs4+w3tes4)/2 if w3tms4==.
gen test2wkhd=(w3tcs2+w3tes2+w3tms2)/3
gen test2hw=(w3tcs3+w3tes3+w3tms3)/3
gen test2askans=(w3tcs4+w3tes4+w3tms4)/3
replace w3p201=. if w3p201==97|w3p201==99
replace w3s460=. if w3s460==97|w3s460==99
replace w4td07=. if w4td07==97|w4td07==99
replace w4td06=. if w4td06==97|w4td06==99
replace w4p225=. if w4p225==97|w4p225==99
replace w4dtc08=. if w4dtc08==97|w4dtc08==99
replace w3dtc08=. if w3dtc08==97|w3dtc08==99
replace w3dtc08=w4dtc08 if w3dtc08==.
replace w4dtc08=w3dtc08 if w4dtc08==.
gen tefelparpreure=( w3dtc08+ w4dtc08)/2
replace w4p229=. if w4p229==97|w4p229==99
replace w4td05=. if w4td05==97|w4td05==99
replace w3td08=. if w3td08==97|w3td08==99
replace w3td07=. if w3td07==97|w3td07==99
replace w3td08=w4td03 if w3td08==.
replace w4td03=w3td08 if w4td03==.
gen teselfdispil= (w4td03+ w3td08)/2
replace w3s104=. if w3s104==97|w3s104==99
replace w3p212=. if w3p212==97|w3p212==99
replace w3p209=. if w3p209==97|w3p209==99
replace w4p226=. if w4p226==97|w4p226==99
replace w3s121=. if w3s121==97|w3s121==99
replace w3s322=. if w3s322==97|w3s322==99
replace w3s320=. if w3s320==97|w3s320==99
replace w3s315=. if w3s315==97|w3s315==99
replace w3s313=. if w3s313==97|w3s313==99
replace w3s313=w3s320 if w3s313==.
replace w3s320=w3s313 if w3s320==.
replace w3s315=w3s322 if w3s315==.
replace w3s322=w3s315 if w3s322==.
gen fmhm=(w3s315+w3s322)/2
gen workstudydisc=(w3s313+w3s320)/2
replace w4p208=. if w4p208==97|w4p208==99
replace w4p207=. if w4p207==97|w4p207==99
replace w4dtc11=. if w4dtc11==97|w4dtc11==99
replace w4mtc09=. if w4mtc09==97|w4mtc09==99
replace w3s313=. if w3s313==97|w3s313==99
egen teacher3askscore= rowmean(w4ctc09 w4etc09 w4mtc09 w4dtc11)
replace w3ctc06=. if w3ctc06==97|w3ctc06==99
replace w3mtc06=. if w3mtc06==97|w3mtc06==99
replace w3etc06=. if w3etc06==97|w3etc06==99
egen teacher2askscore= rowmean(w3ctc06 w3mtc06 w3etc06)
replace w4dtc03=. if w4dtc03==97|w4dtc03==99
replace w4mtc07=. if w4mtc07==97|w4mtc07==99
replace w4ctc07=. if w4ctc07==97|w4ctc07==99
replace w4etc07=. if w4etc07==97|w4etc07==99
replace w3dtc03=. if w3dtc03==97|w3dtc03==99
replace w3mtc05=. if w3mtc05==97|w3mtc05==99
replace w3etc05=. if w3etc05==97|w3etc05==99
replace w3ctc05=. if w3ctc05==97|w3ctc05==99
egen teacher2classlevel= rowmean(w3dtc03 w3mtc05 w3etc05 w3ctc05)
egen teacher3classlevel= rowmean(w4dtc03 w4mtc07 w4etc07 w4ctc07)
replace w3ctc20=. if w3ctc20==97|w3ctc20==99
replace w3ctc21=. if w3ctc21==97|w3ctc21==99
replace w3etc20=. if w3etc20==97|w3etc20==99
replace w3etc21=. if w3etc21==97|w3etc21==99
replace w3mtc20=. if w3mtc20==97|w3mtc20==99
replace w3mtc21=. if w3mtc21==97|w3mtc21==99
replace w4ctc28=. if w4ctc28==97|w4ctc28==99
replace w4ctc29=. if w4ctc29==97|w4ctc29==99
replace w4etc28=. if w4etc28==97|w4etc28==99
replace w4etc29=. if w4etc29==97|w4etc29==99
replace w4mtc28=. if w4mtc28==97|w4mtc28==99
replace w4mtc29=. if w4mtc29==97|w4mtc29==99
egen teacher2classtest= rowmean(w3ctc20 w3etc20 w3mtc20)
egen teacher2classhw= rowmean(w3ctc21 w3etc21 w3mtc21)
egen teacher3classtest= rowmean(w4ctc28 w4etc28 w4mtc28)
egen teacher3classhw= rowmean(w4ctc29 w4etc29 w4mtc29) 
replace w4mtc24=. if w4mtc24==97|w4mtc24==99
replace w4etc24=. if w4etc24==97|w4etc24==99
replace w4ctc24=. if w4ctc24==97|w4ctc24==99
replace w3etc16=. if w3etc16==97|w3etc16==99
replace w3mtc16=. if w3mtc16==97|w3mtc16==99
replace w3ctc16=. if w3ctc16==97|w3ctc16==99
replace w4t217=. if w4t217==97|w4t217==99
replace w4t216=. if w4t216==97|w4t216==99
replace w3t317=. if w3t317==97|w3t317==99
replace w3t316=. if w3t316==97|w3t316==99
replace w3t311=. if w3t311==97|w3t311==99
egen teacher2order= rowmean(w3etc16 w3mtc16 w3ctc16)
egen teacher3order= rowmean(w4etc24 w4mtc24 w4ctc24)
egen teacherlevelnequal= rowmean(w3t317 w4t217)
egen teacherngoodlevel= rowmean(w4t216 w3t316)
replace crammathhelp=. if crammathhelp==97|crammathhelp==99
replace commuschol=. if commuschol==97|commuschol==99
replace w3t317=. if w3t317==97|w3t317==99
replace w3t316=. if w3t316==97|w3t316==99
replace w3t311=. if w3t311==97|w3t311==99
replace w4s314=. if w4s314==97|w4s314==99
replace w4s315=. if w4s315==97|w4s315==99
replace w4s319=. if w4s319==97|w4s319==99
replace w3p602=. if w3p602==97|w3p602==99
replace w4s444=. if w4s444==97|w4s444==99
replace w4s451=. if w4s451==97|w4s451==99
replace w4s452=. if w4s452==97|w4s452==99
replace w4s453=. if w4s453==97|w4s453==99
replace w4s455=. if w4s455==97|w4s455==99
replace w4s456=. if w4s456==97|w4s456==99
replace w4s457=. if w4s457==97|w4s457==99
replace w4s458=. if w4s458==97|w4s458==99
replace w4s459=. if w4s459==97|w4s459==99
replace w4s409=. if w4s409==97|w4s409==99
replace w4s335=. if w4s335==97|w4s335==99
replace w3s4574=. if w3s4574==97|w3s4574==99
replace beforecram =. if beforecram ==297
replace cthm=17 if cthm==116
replace mahm=17 if mahm==116
replace mahm=15 if mahm==213
replace mahm=. if mahm==499
replace mahm=. if mahm==594
replace w3s106=. if w3s106==97|w3s106==99
label variable careclasstime "學校課輔時間"
label variable test2wkhd "二年級老師評量學生努力"
label variable test2hw "二年級老師評量學生作業"
label variable test2askans "二年級老師評量學生主動回答"
label variable tefelparpreure "老師感覺家長給的升學壓力"
label variable teacherngoodlevel "老師擔心學生程度"
label variable teacherlevelnequal "老師擔心學生程度不均"
label variable teacher3order "老師三年級管秩序"
label variable teacher2order "老師二年級管秩序"
label variable teacher3classhw "老師三年級作業"
label variable teacher3classtest "老師三年級考試"
label variable teacher2classhw "老師二年級作業"
label variable teacher2classtest "老師二年級考試"
label variable teacher3classlevel "老師三年級感覺班級程度"
label variable teacher2classlevel "老師二年級感覺班級程度"
label variable teacher2askscore "老師二年級要求成績"
label variable teacher3askscore "老師三年級要求成績"
label variable fmhm "家人看功課"
label variable workstudydisc "工作升學跟家長討論"
label variable teselfdispil "老師感覺學生自律程度"
drop if w4refuse==1
replace cram12=1 if cram12==100
replace cram3=1 if cram3==100
replace cram12=0 if cram12==99
replace cram3=0 if cram3==99
replace cram12=. if cram12==198
replace cram3=. if cram3==198
egen cramdum=rowtotal(cramnum cram12 cram3)
replace cramdum=1 if cramdum>=1
drop w4s3243 w4s3244 w4s3245 w4etc321 w4etc322 w4etc323 w4etc324 w4etc325 w4ctc321 w4ctc322 w4ctc323 w4ctc324 w4ctc325 w4mtc321 w4mtc322 w4mtc323 w4mtc324 w4mtc325 w4dtc151 w4dtc152 ///
w4dtc153 w4dtc154 w4dtc155 w3ctc20 w3ctc21 w3etc20 w3etc21 w3mtc20 w3mtc21 w4ctc28 w4ctc29 w4etc28 w4etc29 w4mtc28 w4mtc29 w3td08 w4td03 w3s126 w4s106 w3ctc30 w3ctc31 w3ctc32 w3ctc33 w3ctc34 ///
w3ctc35 w3etc30 w3etc31 w3etc32 w3etc33 w3etc34 w3etc35 w3mtc30 w3mtc31 w3mtc32 w3mtc33 w3mtc34 w3mtc35 w3tcs2 w3tcs3 w3tcs4 w3tes2 w3tes3 w3tes4 w3tms2 w3tms3 w3tms4 w3ctc06 w3etc06 w3mtc06 ///
w3etc36 w3etc40 w3mtc36 w3mtc40 w3ctc36 w3ctc40 w4s3282 w4s3283 w4s3284 w4s3285 w4s3262 w4s3263 w4s3264 w4s3265 w3pgrm w3clspgm w4pgrm w4clspgm w4h387a w4h387b w4h388a w4h388b w4h6231 w4h6251 ///
w4h6252 w4h6253 w4h6254 w4h6255 w4h6256 w4h6258 w4ctc09 w4etc09 w4mtc09 w4dtc11 w3ctc05 w3etc05 w3mtc05 w3dtc03 w4etc07 w4ctc07 w4mtc07 w4dtc03 w4s411 w4s412 w4s413 w4h3631 w4h3632 w4h3634 w4h3272 ///
w4h3273 w4h3274 w3s313 w3s315 w3s320 w3s322 w3p701 w3p711 w3p712 w4p316 w4p317 w4s407 w4s402 w4p421 w4p422 w4p2333 w4p2334 w4p2335 w3p705 w4p404 w4p107 w3p107 w3fahlth w3mohlth w3p110 w4p110 ///
w4p2141 w4p2146 w3dtc08 w4dtc08 w4s1131 w4s1132 w4s1133 w4s1141 w4s1142 w4s1143 w4s1121 w4s1122 w4s1123 w3t316 w3t317 w4t216 w4t217 w3ctc16 w3mtc16 w3etc16 w4ctc24 w4etc24 w4mtc24 w4p318 w4p319 w4s110 ///
w4s111 w4s1134 w4s1135 w4s1144 w4s1145 w4s1281 w4s1282 w4s1284 w4s1283 w4s1285 w3s3281 w3s3282 w3s3283 w3refuse w4refuse w4s104 w4s105 w4faedu w4moedu w3p605 w3p713 w4s1081 w4s1082 w4s1083 w4s102 w4s103 ///
w4s1152 w4s1153 w4s1154 w3chin_id w3ctch_id w4chin_id w4ctch_id w4engl_id w4etch_id w4math_id w4mtch_id w3faocc w3faindu w3moocc w3moindu w3p709 w3p710 w3p512 w3p513 w3cls_id w4cls_id w4dtch_id w3p604 ///
w3s427 w3s425 w3s426 w4p414 w4p234
order stud_id w1s502 w3s480 w3s415 w4s449 w4s450 w3s101 w4s1292 w4s1293 w4s1294 w4s1301 w4s1302 w4s1303 w4s1304 w4s1305 w3sch_id w4sch_id w3s213 track w3priv w3urban3 w3w4chg w4priv w4urban3 w4scarea w4admarea ///
indrs g1a g2a g3a coretotal cramnum cramdum cram12 cram3 w3s106 w4h1031 w4h319a w4h320a w4h362 w4h364 w4h365 w4h410 paredu scenhan scunipub scaward schelpcla scteamatt outclubatt beforecram ctclag mtclag ///
etclag teststre stubestcl freecram ctcfor3 etcfor3 mtcfor3 dtcfor3 loan teclear w3s3315 teachcare classinter w3s3284 w3s3285 w4s2075 w4s2085 w4s2095 w4s2105 w4s2115 familyhealthcare w4s2065 discussenroll ///
cthm mahm w4s444 w4s451 w4s452 w4s453 w4s455 w4s456 w4s457 w4s458 w4s459 w4s409 w4s335 w3s4574 w4dtc13 w3t4063 w4s314 w4s315 w4s319 w3p602 commuschol enhm w4p202 crammathhelp parentmathcramhelp w3t311 w4p207 ///
w4p208 w4p209 w3dtc09 w3dtc13 w3s121 w4p226 w3p209 w3p212 w3s104 w3td07 w4td05 w4p229 w3dtc14 w4p225 w4td06 w4td07 w3p201 w3s460 careclasstime test2wkhd test2hw test2askans tefelparpreure teselfdispil fmhm ///
workstudydisc teacher3askscore teacher2askscore teacher2classlevel teacher3classlevel teacher2classtest teacher2classhw teacher3classtest teacher3classhw teacher2order teacher3order teacherlevelnequal teacherngoodlevel 
egen tclag=rowmean(etclag ctclag mtclag)
replace dtcfor3=. if dtcfor3==485
egen for3=rowmean(ctcfor3 mtcfor3 etcfor3 dtcfor3)
drop etclag ctclag mtclag ctcfor3 mtcfor3 etcfor3 dtcfor3 w4s3221 w4s3222 w4s3223 w4s3224 w4s3225 w4s3226 w4s336 w4h147 w4h3271 wfaedu wmoedu ctclag2 ctclag3 etclag2 mtclag2 etclag3 mtclag3
drop w3s111 w4ctc04 w4etc04 w4p2143 w4p412 w4p413 w4p423 w4p424
label variable tclag "落後學生措施"
label variable for3 "三年級考試措施"
label variable paredu "家長教育程度"
label variable scenhan "學校提升成績措施"
label variable scunipub "公立大學升學率"
label variable scaward "學校成績頒獎"
label variable schelpcla "補救教學班級"
label variable scteamatt "學生校隊參與"
label variable outclubatt "學生校外社團參與"
label variable beforecram "學生先前補習經驗"
label variable teststre "學生準備考試技巧"
label variable stubestcl "學生資優班"
label variable freecram "想補科目數"
label variable loan "學生貸款"
label variable teclear "老師講解清楚"
label variable teachcare "老師關心學生學習"
label variable classinter "老師互動"
label variable crammathhelp "學生覺得補數學幫助"
label variable parentmathcramhelp "家長覺得補數學幫助"
order w4p202 crammathhelp parentmathcramhelp freecram, after( cram3 )

sum coretotal cramdum cramnum
sum coretotal cramdum cramnum if w1s502==1
sum coretotal cramdum cramnum if w1s502==2
sum coretotal cramdum cramnum if w4priv==0
sum coretotal cramdum cramnum if w4priv==1
      
reg coretotal cramnum w3s106 - for3 ,r
pdslasso coretotal cramnum (w3s106 - for3),rob
rlasso coretotal w3s106 - for3,rob
rlasso cramnum w3s106 - for3,rob
reg coretotal cramnum w4h362 w4h364 w4h365 paredu scunipub scteamatt teststre stubestcl loan teclear w3s3315 w4s458 w4s409 w4s335 w3s4574 w4s319 ///
 w3p602 w3t311 w4p207 w4p208 w3td07 w4td05 w4p229 w3dtc14 w4p225 w3p201 test2wkhd test2askans workstudydisc teacher2askscore teacher3classlevel ///
 teacher2classhw teacher3classtest teacher2order teacher3order teacherlevelnequal teacherngoodlevel

reg coretotal cramnum w3s106 - for3 if w1s502==1 ,r
pdslasso coretotal cramnum (w3s106 - for3) if w1s502==1,rob
rlasso coretotal w3s106 - for3 if w1s502==1,rob
rlasso cramnum w3s106 - for3 if w1s502==1,rob
reg coretotal cramnum w4h362 w4h365 paredu scunipub scteamatt teststre stubestcl loan w3s3315 classinter w4s458 w4s409 w3s4574 w4dtc13 w4s319 w3p602 w3t311 ///
  w4p207 w4p208 w3td07 w4td05 w4p229 test2wkhd test2askans teacher2askscore teacher3classlevel teacher3classtest teacher2order  teacher3order teacherngoodlevel ///
  if w1s502==1,r

reg coretotal cramnum w3s106 - for3 if w1s502==2 ,r
pdslasso coretotal cramnum (w3s106 - for3) if w1s502==2,rob
rlasso coretotal w3s106 - for3 if w1s502==2,rob
rlasso cramnum w3s106 - for3 if w1s502==2,rob
reg coretotal cramnum w4h362 w4h364 w4h365 paredu scunipub scteamatt teststre stubestcl w3s3315 w4s458 w4s409 w3s4574 w3p602 w4p207 w4p208 w3td07 ///
 w4td05 w3dtc14 w4p225 w3p201 test2wkhd test2askans workstudydisc teacher2askscore teacher3classlevel teacher2classhw teacher3classtest teacher2order teacher3order teacherngoodlevel if w1s502==2,r

reg coretotal cramnum w3s106 - for3 if w4priv==0 ,r
pdslasso coretotal cramnum (w3s106 - for3) if w4priv==0,rob
rlasso coretotal w3s106 - for3 if w4priv==0,rob
rlasso cramnum w3s106 - for3 if w4priv==0,rob
reg coretotal cramnum w4h362 w4h364 w4h365 paredu scunipub scteamatt teststre stubestcl w3s3315 w4s458 w4s409 w4s335 w3s4574 w3p602 w4p207 w4p208 w3td07 w4td05 ///
w4p229 w4p225 w3p201 test2wkhd test2askans workstudydisc teacher2askscore teacher2classlevel teacher3classlevel teacher2classhw teacher3classtest teacher2order ///
teacher3order teacherngoodlevel if w4priv==0,rob

reg coretotal cramnum w3s106 - for3 if w4priv==1 ,r
pdslasso coretotal cramnum (w3s106 - for3) if w4priv==1,rob
rlasso coretotal w3s106 - for3 if w4priv==1,rob
rlasso cramnum w3s106 - for3 if w4priv==1,rob
reg coretotal cramnum w4h364 w4h410 paredu scunipub scaward teststre stubestcl w3s3285 w4s409 w3s4574 w3p602 w3t311 w4p207 w4p208 w3td07 w4td05 w3dtc14 /// 
careclasstime test2wkhd test2askans teacher2askscore teacher3classlevel teacher2order teacher3order teacherngoodlevel tclag if w4priv==1,rob

reg coretotal cramdum w3s106 - for3 ,r
pdslasso coretotal cramdum (w3s106 - for3),rob
rlasso coretotal w3s106 - for3,rob
rlasso cramdum w3s106 - for3,rob
reg coretotal cramdum w3s106 w4h362 w4h364 w4h365 paredu scunipub scteamatt teststre stubestcl loan teclear w3s3315 w4s458 w4s409 w4s335 w3s4574 w4s319 w3p602 w3t311 w4p207  ///
 w4p208 w4p226 w3p209 w3td07 w4td05 w4p229 w3dtc14 w3p201 test2wkhd test2askans teselfdispil workstudydisc teacher2askscore teacher3classlevel teacher2classhw ///
 teacher3classtest teacher2order teacher3order teacherlevelnequal teacherngoodlevel,r

reg coretotal cramdum w3s106 - for3 if w1s502==1 ,r
pdslasso coretotal cramdum (w3s106 - for3) if w1s502==1,rob
rlasso coretotal w3s106 - for3 if w1s502==1,rob
rlasso cramdum w3s106 - for3 if w1s502==1,rob 
reg coretotal cramdum w4h362 w4h365 paredu scunipub scteamatt teststre stubestcl loan w3s3315 classinter w4s458 w4s409 w3s4574 w4dtc13 w4s319 w3p602 w3t311 w4p207 w4p208 w3p209 ///
w3td07 w4td05 w4p229 test2wkhd test2askans teselfdispil teacher2askscore teacher3classlevel teacher3classtest teacher2order teacher3order teacherngoodlevel if w1s502==1,rob 

reg coretotal cramdum w3s106 - for3 if w1s502==2 ,r
pdslasso coretotal cramdum (w3s106 - for3) if w1s502==2,rob
rlasso coretotal w3s106 - for3 if w1s502==2,rob
rlasso cramdum w3s106 - for3 if w1s502==2,rob 
reg coretotal cramdum w4h362 w4h364 w4h365 paredu scunipub scteamatt teststre stubestcl loan w3s3315 w4s458 w4s409 w3s4574 w3p602 w4p207 w4p208 w3td07 w4td05 w3dtc14 w3p201 test2wkhd test2askans ///
 workstudydisc teacher2askscore teacher3classlevel teacher2classhw teacher3classtest teacher2order teacher3order teacherngoodlevel if w1s502==2,rob 

reg coretotal cramdum w3s106 - for3 if w4priv==0 ,r
pdslasso coretotal cramdum (w3s106 - for3) if w4priv==0,rob
rlasso coretotal w3s106 - for3 if w4priv==0,rob
rlasso cramdum w3s106 - for3 if w4priv==0,rob
reg coretotal cramdum  w4h362 w4h364 w4h365 paredu scunipub scteamatt teststre stubestcl w3s3315 w4s458 w4s409 w4s335 w3s4574 w3p602 w4p207 w4p208 w3p209 w3td07 w4td05 w4p229 w3p201 test2wkhd ///
test2askans teselfdispil workstudydisc teacher2askscore teacher2classlevel teacher3classlevel teacher2classhw teacher3classtest teacher2order teacher3order teacherngoodlevel if w4priv==0

reg coretotal cramdum w3s106 - for3 if w4priv==1 ,r
pdslasso coretotal cramdum (w3s106 - for3) if w4priv==1,rob
rlasso coretotal w3s106 - for3 if w4priv==1,rob
rlasso cramdum w3s106 - for3 if w4priv==1,rob
reg coretotal cramdum  w3s106 w4h364 w4h410 paredu scunipub scaward teststre stubestcl loan w3s3285 w4s409 w3s4574 w3p602 w3t311 w4p207 w4p208 w3td07 w4td05 w3dtc14 careclasstime test2wkhd /// 
test2askans teacher2askscore teacher3classlevel teacher2order teacher3order teacherngoodlevel tclag if w4priv==1 ,r
