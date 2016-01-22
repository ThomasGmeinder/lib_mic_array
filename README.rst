Microphone array library
========================

.. rheader::

   Microphone array library |version|

Microphone array library
------------------------

The XMOS microphone array library is designed to allow interfacing to PDM 
microphones coupled with efficient decimation to user selectable output
sample rates. Additionally, a high resolution delay can be introduced to 
each of the individual PDM microphones allowing for individual time shifts.

Features
........

The microphone array library has the following features:

  - 48kHz, 24kHz, 16kHz, 12kHz and 8kHz output sample rate by default (3.072MHz PDM clock), 
  - 44.1kHz, 22.05kHz, 14.7kHz, 11.025kHz and 7.35kHz output sample rate by default (2.8224MHz PDM clock), 
  - 4, 8, 12 or 16 PDM interfaces per tile,
  - Minimum of 100dB of signal to noise for all output sample frequencies,
  - Configurable latency, ripple and bandwidth .
  - Framing, configurable frame size from 1 sample to 4096 samples plus 50% overlapping frames option.
  - Windowing and sample index bit reversal within a frame.
  - Individual microphone gain compensation,
  - DC bias removal,
  - Up to 3.072MHz input sample rate,
  - High resolution (1.3 microsecond) microphone specific delay lines.

Components
...........

 * PDM interface
 * Four channel decimators
 * High resolution delay block
 
 Known Issues
............

 * Data from mic pairs 1/2 and 5/6 are swapped from expected ordering. i.e. indices 1/2 and 5/6 of frame_audio.data[] (#17167)
   
Software version and dependencies
.................................

.. libdeps::

Related application notes
.........................

None
