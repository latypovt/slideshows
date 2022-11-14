---
layout: default
title: TN Grades
permalink: /grades
---


            <h5>Medication relief</h5>
	    <input type="radio" name="med_relief" id="med_relief_yes" />
	    <label for="med_relief_yes">yes</label> 
	    <input type="radio" name="med_relief" id="med_relief_no" />
	    <label for="med_relief_no">no</label> 
	    <br>
            <h5>Frequency of pain episodes</h5>
            <br>
	    <input type="radio" name="attacks" id="no_attacks" />
	    <label for="no_attacks">Rare attacks?</label> 
	    <input type="radio" name="attacks" id="seasonal_attacks" />
	    <label for="seasonal_attacks">Seasonal attacks?</label> 
	    <input type="radio" name="attacks" id="monthly_attacks" />
	    <label for="monthly_attacks">Monthly attacks?</label> 
	    <input type="radio" name="attacks" id="weekly_attacks" />
	    <label for="weekly_attacks">Weekly attacks?</label> 
	    <input type="radio" name="attacks" id="daily_attacks" />
	    <label for="daily_attacks">Daily attacks?</label> 
	    <input type="radio" name="attacks" id="multiple_attacks" />
	    <label for="multiple_attacks">Multiple attacks per day?</label> 
	    <input type="radio" name="attacks" id="constant_pain" />
	    <label for="constant_pain">Constant pain?</label> 
	    <br>
            <h5>Sex of the patient</h5>
            <br>
	    <input type="radio" name="sex" id="sex_female" />
	    <label for="sex_female">female</label> 
	    <input type="radio" name="sex" id="sex_male" />
	    <label for="sex_male">male</label> 
	    <br>
	    <h5>Any history of the following</h5>
            <br>
	    <label for="thyroid">Hypothyroidism</label> 
	    <input type="checkbox" name="thyroid" id="thyroid" />
	    <br>
	    <label for="diabetes">Diabetes Type II</label> 
	    <input type="checkbox" name="diabetes" id="diabetes" />
	    <br>
	    <label for="cancer">Cancer</label> 
	    <input type="checkbox" name="cancer" id="cancer" />
	    <br>
	    <label for="muskuloskeletal">Arthritis</label> 
	    <input type="checkbox" name="muskuloskeletal" id="muskuloskeletal" />
	    <br>
	    <label for="psychiatric">Depression / Anxiety</label> 
	    <input type="checkbox" name="psychiatric" id="psychiatric" />
	    <br>
	    <h5>Pain description</h5>
            <br>
	    <label for="electric_pain">Pain is electric shock-like</label> 
	    <input type="checkbox" name="electric_pain" id="electric_pain" />
	    <br>
	    <label for="triggers">Pain is occurring spontaneously (no triggers)</label> 
	    <input type="checkbox" name="triggers" id="triggers" />
	    <br>
	    <label for="trigeminal_deficit">Increased / decreased sensitivity in the area of CN-V</label> 
	    <input type="checkbox" name="trigeminal_deficit" id="trigeminal_deficit" />
	    <br>
            <h5>Age</h5>
	    <input type="number" name="age" id="age" />
	    <label for="age">in years</label> 
	    <br>
            <h5>Side of pain</h5>
	    <input type="radio" name="pain_side" id="pain_side_right" />
	    <label for="pain_side_right">Right</label> 
	    <input type="radio" name="pain_side" id="pain_side_left" />
	    <label for="pain_side_left">Left</label> 
	    <br>
	    <input type="button" value="Get pain stage" onclick="test();"/>

