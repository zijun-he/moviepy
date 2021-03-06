.. ref_audiofx:

************
audio.fx
************


The module ``moviepy.audio.fx`` regroups functions meant to be used with ``audio.fx()``.
Note that some of these functions such as ``multiply_volume`` (which multiplies the volume) can
be applied directly to a video clip, at which case they will affect the audio clip attached to this
video clip. Read the docs of the different functions to know when this is the case.

Because this module will be larger in the future, it allows two kinds of import.
You can either import a single function like this: ::
    
    from moviepy.audio.fx.multiply_volume import multiply_volume
    newaudio = audioclip.fx(multiply_volume, 0.5)

Or import everything: ::
    
    import moviepy.audio.fx.all as afx
    newaudio = (audioclip.afx( vfx.normalize)
                         .afx( vfx.multiply_volume, 0.5)
                         .afx( vfx.audio_fadein, 1.0)
                         .afx( vfx.audio_fadeout, 1.0))



When you type ::
    
    from moviepy import *

the module ``audio.fx`` is loaded as ``afx`` and you can use ``afx.multiply_volume``, etc.


.. currentmodule:: moviepy.audio.fx.all

.. autosummary::
    :toctree: audiofx
    :nosignatures:
    
    audio_delay
    audio_fadein
    audio_fadeout
    audio_normalize
    multiply_stereo_volume
    multiply_volume
