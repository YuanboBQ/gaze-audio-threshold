Keyboard Commands:

You can exit the program by holding down the escape key 'ESC'. Depending
on where you are in the experiment you may have to hold for a few seconds before exit.

You can calibrate at anytime by holding down the 'c' key (c for calibrate). Depending
on where you are in the experiment you may have to hold for a few seconds before it starts.
Please note the calibration is followed by a validation. The results from this validation will
overwrite any prior validation info.

Press 't' to pause & 'y' to unpause

To play an attention movie use 'p' to play and 's' to stop


-------------------------------------------------------------------------------

Here are some notes on the data files, the variables each file has consist of:

Calib  info on eye tracker & viewing screen

Constants  experimental constants

CorrectLocation  Which side is the correct side per trial (0 left, 1 right)

EyeData  eye info struct containts
	    leye_xypv  - left eye x,y, pupil, validity code
    reye_xypv  right eye    
    AOI  AOI detection, column 1=left, 2=right, 3=fixation point, rows=eye tracking frames
    Time  time in seconds for each eye data frame
            
EyeErrorTestStart : struct containing fairly obvious contents
    Left  x,y
    Right  x,y
    Left_TrackLoss
    Right_TrackLoss
    Left_Validity
    Right_Validity
    Left_pupil
    Right_pupil

TrialData          (contains stimulus timing info, in seconds, same clock as EyeData.time)
   AudioPlayTime  when did the sound start playing?
    VisStimAppearTime  when did the Left & right boxes appear

trialScore         - was the subject right (1) or wrong (0)

Note the above applies to Training trials 1 & 2, Trial 3 also has:

AudioStimList  which audio stimulus was played, either 0=low or 1=high,  in this case you can think of low & high referencing the number
In the audio file name as they are sound1.wav to sound11.wav, so low means low number & high means high number.  Note in the full experiment
We also have step size info(see below)

In the FullExp we have:

EyeErrorTestEnd  same format as error test begin

PerfCode = Code describing why the experiment was brought to an end
1, max performance, 2 minimum performance, 3  exceeded maximum number of reversals

ReversalCount  how many reversals did they have

StepStimulus  at what level was the non-static stimulus per trial?
