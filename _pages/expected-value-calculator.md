---
layout: page
title: Expected Value Calculator
meta_title: Expected Value Calculator
permalink: /expected-value-calculator/
---

<!--
 TODO
 Alpha
 - Setup keyword monitoring

 Later
 - Did you find this helpful?
-->

<style type="text/css">
  .evc {
    margin-top: 18px;
    margin-bottom: 24px;
  }

  .evc .form-fields {
    background-color: #eee;
    padding: 10px;
    clear: both;
    width: 390px;
  }

  .evc fieldset {
    border: none;
    padding: 0;
  }
  .evc legend {
    padding: 0;
    margin: 0 0 18px 0;
    display: block;
  }
  .evc label {
    width: 200px;
    float: left;
  }

  .evc input {
    font-size: 16px;
    padding: 3px 5px 3px 5px;
  }

  .evc .form-group {
    display: block;
    overflow: hidden;
    margin-bottom: 9px;
  }

  .evc .form-group:last-child {
    margin-bottom: 0;
  }

  .evc__result-panel {
    margin-top: 18px;
    font-weight: 700;
  }
</style>

<form class="evc">
  <fieldset>
    <legend>This calculator will tell you the <strong>expected value</strong> for a binomial random variable, given the value and probability of success.</legend>
    <div class="form-fields">
      <div class="form-group">
        <label>Probability of success:</label>
        <input type="number" value="0.1" min="0" max="1" step="0.1" id="evc__probability-success" name="evc__probability-success" class="form-control">
      </div>
      <div class="form-group">
        <label>Value of success, or number of trials:</label>
        <input type="number" value="1" id="evc__trials" min="1" name="evc__trials" class="form-control">
      </div>
      <div class="form-group evc__result-panel">
        <label>Expected value:</label> <span id="evc__result">0.1</span>
      </div>
    </div>
  </fieldset>
</form>

<hr>
<h3>Formula used</h3>
<p>This calculator uses the following formula to calculate expected value for a binomial random variable:</p>
<blockquote>E(x) = np</blockquote>
<p>Where <em>n</em> is the value of success or number of trials, and <em>p</em> is the probability of success.</p>
<h3>What is expected value?</h3>
<p>Expected value is statistical concept which is often used as a tool for thinking about risk. You can learn more about expected value on <a href="https://www.khanacademy.org/math/probability/random-variables-topic/expected-value">Kahn Academy</a> or <a href="https://en.wikipedia.org/wiki/Expected_value" target="_blank">Wikipedia</a>.</p>

<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/zepto/1.1.6/zepto.js"></script>

<script>
  var $result = $('#evc__result');
  var $trials = $('#evc__trials');
  var $probabilitySuccess = $('#evc__probability-success');

  $trials.on('change', function() {
    updateResult();
  });

  $probabilitySuccess.on('change', function() {
    updateResult();
  });

  function updateResult() {
    var trials = parseFloat($trials.val());
    var probabilitySuccess = parseFloat($probabilitySuccess.val());
    if(probabilitySuccess > 1) {
      probabilitySuccess = 1;
      $probabilitySuccess.val(1);
    }
    var exactResult = trials * probabilitySuccess;
    var result = Math.round(exactResult * 100) / 100;
    console.log($trials.length);
    console.log(trials);
    console.log(probabilitySuccess);
    if(!isNaN(result)) {
      $result.html(result);
    }

    analytics.track('Updated calculation');
  }
</script>