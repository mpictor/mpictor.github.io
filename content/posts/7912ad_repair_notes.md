+++
date = 2025-09-27T00:42:38-05:00
draft = false
title = '7912AD repair notes'
+++

### Setup
* [7912AD](https://w140.com/tekwiki/wiki/7912AD)
* 7A19 amplifier
* 7B92A timebase
* TV attached to LINEAR COMP OUT
* extra cooling (when lid off) via 120mm pc fan, over A16-A28
* signal generator as needed

### Symptoms

* no trace or graticule drawn on TV, regardless of intensity settings
* scale factors (from the character generator) _are_ drawn
* turning up either intensity knob activates the `decrease intensity` indicator, as expected
* 7B92A can bypass intensity limits (!)
  * use caution: apparently, excessive intensity can quickly damage the scan converter
  * configure timebase for `ALT SWEEP` (pull knob)
  * `ALT INTEN` bypasses limits and can be bright enough to be seen
  * expected waveforms are visible this way
  * drives Z-axis signal beyond limits otherwise imposed
  * is this by design?
* did see trace in past - what changed?

### Checks performed so far

* intensity limits (pg 5-43)
  * involves attaching to z-axis output signal, A40 TP844
  * this signal unblanks for trace and graticule
  * signal shape and magnitude as depicted in manual
  * exception: 7B92A alt sweep, above
* horiz deflection
  * active for both trace and graticule
  * amplitude assumed to be acceptable (did not check manual)
* vert deflection
  * likewise

### Conclusions so far

* horizontal and vertical seem functional
  * backed up by waveform visibility with ALT INTEN
* Z seems functional to Z amp output
  * have not checked HV output: need a probe safe for 10kV +

### Next steps
* acquire HV probe for DMM and/or scope
* problem likely lies with
  * HV misadjustment (A40)
  * defective HV osc (A72) or 10kV assembly (A74)
* likely _not_ the scan converter
* intensity bypass in `ALT` mode: is this by design?

## To be continued...
