---
title: "BiquadFilterNode: gain property"
short-title: gain
slug: Web/API/BiquadFilterNode/gain
page-type: web-api-instance-property
browser-compat: api.BiquadFilterNode.gain
---

{{ APIRef("Web Audio API") }}

The `gain` property of the {{ domxref("BiquadFilterNode") }} interface is an [a-rate](/en-US/docs/Web/API/AudioParam#a-rate) {{domxref("AudioParam")}} — a double representing the [gain](https://en.wikipedia.org/wiki/Gain) used in the current filtering algorithm.

When its value is positive, it represents a real gain; when negative, it represents an attenuation.

It is expressed in dB, has a default value of `0`, and can take a value in a nominal range of `-40` to `40`.

## Value

An {{domxref("AudioParam")}}.

> [!NOTE]
> Though the `AudioParam` returned is read-only, the value it represents is not.

## Examples

The following example shows basic usage of an AudioContext to create a Biquad filter node.
For more complete applied examples/information, check out our [Voice-change-O-matic](https://github.com/mdn/webaudio-examples/tree/main/voice-change-o-matic) demo (see [app.js lines 108–193](https://github.com/mdn/webaudio-examples/blob/main/voice-change-o-matic/scripts/app.js#L108-L193) for relevant code).

```js
const audioCtx = new AudioContext();

// Set up the different audio nodes we will use for the app
const analyser = audioCtx.createAnalyser();
const distortion = audioCtx.createWaveShaper();
const gainNode = audioCtx.createGain();
const biquadFilter = audioCtx.createBiquadFilter();
const convolver = audioCtx.createConvolver();

// Connect the nodes together

source = audioCtx.createMediaStreamSource(stream);
source.connect(analyser);
analyser.connect(distortion);
distortion.connect(biquadFilter);
biquadFilter.connect(convolver);
convolver.connect(gainNode);
gainNode.connect(audioCtx.destination);

// Manipulate the Biquad filter

biquadFilter.type = "lowshelf";
biquadFilter.frequency.value = 1000;
biquadFilter.gain.value = 25;
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [Using the Web Audio API](/en-US/docs/Web/API/Web_Audio_API/Using_Web_Audio_API)
