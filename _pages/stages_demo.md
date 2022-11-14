---
layout: default
title: TN Grades
permalink: /grades
---


<form onsubmit="test()">
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
	    <label for="musculoskeletal">Arthritis</label> 
	    <input type="checkbox" name="musculoskeletal" id="musculoskeletal" />
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
	    <input type="radio" name="pain_side" id="pain_side_leftt" />
	    <label for="pain_side_leftt">Left</label> 
	    <br>
	    <input type="submit" value="Get pain stage"/>
	  </form>
	  <script>
	    function test() {
              age_mu = 60.3;  // mean of age distribution
              age_sigma = 14.4;  // std dev of age distribution
              weights = {
                  "med_relief": 0.5823305406093363,
                  "no_attacks": 0.4447773784715664,
                  "seasonal_attacks": 0.3780998787882947,
                  "multiple_attacks": -0.24936232801694033,
                  "sex": 0.23271058640658165,
                  "thyroid": 0.22194415044916416,
                  "diabetes": -0.19096074484891587,
                  "constant_pain": -0.18043315680694574,
                  "triggers": -0.17800135417611468,
                  "cancer": -0.13696322854364734,
                  "electric_pain": 0.1328637522659141,
                  "age": 0.07879009081158225,
                  "monthly_attacks": -0.07185119306538153,
                  "muskuloskeletal": -0.05171550838967454,
                  "daily_attacks": 0.042491833983521264,
                  "weekly_attacks": -0.027986269788450466,
                  "pain_side": 0.02259789402761426,
                  "trigeminal_deficit": 0.015018209680008613,
                  "psychiatric": -0.0046296250086506575
              };
//	      alert(`The function 'test' is executed`);
//	      alert(dot(weights, [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19]));
	      alert(dot2(weights, [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19]));
	    }
            function get_value_from_key(key) {
                // TODO: do subcases for each key option
                if (key == "med_relief") {
                    bool_yes = document.getElementById("med_relief_yes").checked;
                    bool_no = document.getElementById("med_relief_no").checked;
                    if (!bool_yes & !bool_no) {
                        alert("Please choose an answer for 'med_relief'!");
                    }
                    else {
                        if (bool_yes) {answer = "yes";} else {answer = "no";}
                        alert("Answer for 'med_relief' is: " + answer);
                    }
                }
            }
            function dot2(w, pat) {
                var result = 0;
                for (var key in w) {
                    if (w.hasOwnProperty(key)) {
                        answer_value = get_value_from_key(key);
                        result += w[key] * answer_value;
                    }
                }
                return result;
            }
            dot = (a, b) => a.map((x, i) => a[i] * b[i]).reduce((m, n) => m + n);
	  </script>