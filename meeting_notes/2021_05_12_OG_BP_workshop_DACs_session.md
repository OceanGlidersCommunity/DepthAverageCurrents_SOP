Welcome to the “Ocean Currents - Standard Operating Practice (SOP)” room.


Co-leads: Alice Pietri, Anthony Bosse, Robert Todd

# Agenda
May 12 Wednesday 
	16:00 - 17:30 CEST / 7:00 - 8:30 PDT / 22:00 - 23:30 AWST
	Ocean Currents SOP: Assign people to paragraphs (A. Pietri, A. Bosse, R. Todd)

Participants: Anthony Bosse, Pierre Testor, Ilker Fer, Bastien Queste, Lucas Merckelbach, Robert Todd, Alice Pietri, Daniel Rudnick, Gerasimi Anastasopoulou, Isabelle Giddy, Jacob Steinberg, Louis Clement, Mathieu Gentil, Matthew Palmer, Nikolaos Zarokanellos, Pedro Diaz, Sebastiaan Swart, Vincent Ma, Gillian Damerell, Callum Rollo, Ria Oelerich, John Allen, Orens de Fommervault, Evi Bourma, Tyler Byrne, JongJin Park, Yumi Song

Now everyone can write and edit!

Everyone is asked to write below a bit about what they have experience in:

Jake Steinberg: Seaglider (and Deepglider) DAC estimation, flight model, regressions to obtain best lift, drag, vehicle mass/volume estimates.  
Gillian Damerell, Seagliders only, operations/piloting, compass calibration dives, using the Frajka-Williams flight model (including regressions)
Bastien Queste: Seaglider and SeaExplorer. Merckelbach and UW flight models, flight model regressions (both RT and DM) w/ emphasis on W, limited ADCP experience


Meeting notes: 

SOP working document: 
DMQC Chapter:


Dan Rudnick : go through the various glider platforms and describe how it is done? give relevant reference

Lucas Merckelbach : how DAC is computed is not in the paper. software gives an idea on how it is done for Slocum


Pierre Testor : document in french about how it’s done -> link : https://www.ego-network.org/dokuwiki/lib/exe/fetch.php?media=private:technotes:calcul_courant.pdf

Robert Todd : Role of manufacturer? to provide details on code

Lucas : knows how it is done precisely for slocum. DAC is not well synchronized in time (it is done at the second series of GPS, should be at the average position of segment)

Ilker Fer : find a document about Slocum (-> Teledyne internal doc)

Dan : Is there any time constant involved in DAC estimate? averaging in the method for Slocum?

Lucas : extrapolation back in time from surface drift. flight model uses pitch angle and dp/dt to measure displacement through water. At inflection point (<11°), measurements are cut. does ignore the angle of attack. Best to redo all calculation offline.

Dan : the goal for glider navigation

Robert : don’t need the best precision for glider navigation

Alice : divide in the SOP into RT DAC estimate by platform and DM best estimate

Robert : Structure of document SOP
introduction, principle, schematics flight of a glider etc
RT, navigation, science needs
prep of the glider prior to deployment
sensors needed for DAC (compass, GPS, CTD)
need to address how to calibrate compass, no GPS calibration, for CTD refer to SOP

Jake Steinberg : breakdown of individual glider parameter required by platforms

Alice : find volunteer for paragraph

Soeren : What are the common things of all gliders? What are specificities to platforms? Alice, Robert agree

Jake : parameter determined at the beginning of the mission vs parameter that evolves during the mission (eg drag because of biofouling)

Ilker : Bennet et al, ref paper (Seaglider)

Jake : not sure this code is actually delivered to Seagliders’ users

Louis : it is not

Robert : what big the difference this adjustment is making?

Jake : DAC estimates can diverge with time after a few 100 of dives…

Anthony : specific to Seaglider, because DAC based on flight model and regression coefficients determined at the beginning of the deployment

Robert : people should know what is happening on their glider in RT. Also should know it is not best estimates.

Gillian Damerell : been operating gliders for years without knowing what’s happening onboard, frustrated… nothing bad worse than bad compass…

Robert : Is SOP also tackling how gliders are dealing with DAC for current-correction steering? Bastien -> operating section?

Dan : Spray flight model, simple use of an angle of attack (dependent on other parameters)

Robert : in case of electronic failure (sensor fails), does DAC survive?

Pierre : Slocum works in RT, Seaglider requires more parameters?

Lucas : Slocum offer you the possibility to choose for an angle of attack (set as a constant)

Pierre : not useful, could introduce bias

Bastien : some platforms don’t have constant pitch angle

Dan : not a bad idea to have constant angle of attack if pitch is constant

Ilker : we should concentrate on what we can do offline in the SOP? if RT manufacturer information on DAC is not available then it is ok

Bastien (chat) : Are flight models actually specific to gliders if you're regressing drag coefficients?

Lucas : it is not so specific to platform

Robert : it is a model that has inherent choices

Bastien : to make it easier, why not pushing for the use of one model? Focus should be what is easiest for users, not necessarily a complete understanding of all models

Soeren : until you can evaluate method (based on error estimate), hard to decide which best

Anthony: If you have common parameters for all gliders, can plug them in to any model

Pierre : OceanGliders format would include technical informations -> make a list of parameter needed to run each model

Dan: how to assess accuracy of DAC. Can do it regardless of flight model. Just do a 180 turn and check the DAC before and after. Described in a paper

Gillian: v important for users can make an informed comparison between flight models

Robert: typically a mission long check. Several turns in deep water with a day of recording either side

Robert: ADCPs: hard. A day of mooring comparison is not enough. Intercomparison is difficult. Need a long time at same spot

Dan: surveys along a line with comparisons at points can be enough for ADCP. Lots of surveys already like this

Pierre (chat) : compass calibration and effect in polar region to describe

Soeren (chat) : list the specific issues related to the environment (Tides, shallow water, deep water etc)

Ilker : deployment north of Svalbard (poor compass)

Bastien : deployment in the far south next to magnetic pole (DAC was an issue)

Gillian : can’t do compass calibration dives anymore in very shallow water… has to do it on land.  Also make certain to correct for magnetic declination.


++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

From Zoom Chat:

Alice Pietri to Everyone (09:38)
geostrophic velocities https://docs.google.com/document/d/1kKOt7kU1noW7EHe3MQFt4pMqZX-Efzdyq3x1PsfYaz8/edit
DAC https://docs.google.com/document/d/1nNtHyG0Lj3y1Le20EqFK9AmtKaUF6El_hAs5LHArSM8/edit
Soeren Thomsen  to Everyone (10:05)
All fine here? Everyone can edit the documents?
Anthony Bosse to Everyone (10:05)
yes it works well now
Bastien Queste to Everyone (10:16)
SeaExplorer doesn't do RT DAC
Soeren Thomsen  to Everyone (10:17)
All fine here?
Me to Everyone (10:17)
yep
Soeren Thomsen  to Everyone (10:18)
just jumping between the two sessions. Someone has to copy past the chat discussion over to the google doc or in the best case make most comments there
Bastien Queste to Everyone (10:18)
sure
optimistic
Nikolaos Zarokanellos to Everyone (10:20)
Great idea!
Soeren Thomsen  to Everyone (10:22)
In the doc!
Bastien Queste to Everyone (10:34)
Considering models can be applied across gliders (with more or less success), is it worth detailing the existing models rather than gliders?
Soeren Thomsen  to Everyone (10:35)
yes
I will jump over to the Data Management session to check all is fine! Have a good session!
Gillian Damerell to Everyone (10:47)
Seaglider are that dumb
Tyler Byrne to Everyone (10:47)
Slocums *can* be that dumb
Bastien Queste to Everyone (10:49)
I would've thought ferry angles/current avoidance would land in the Operations chapter?
Gillian Damerell to Everyone (10:51)
Actually Seagliders can have a failsafe - if they fail to reach a waypoint after a given interval they'll do something different (I forget exactly what - maybe go for the next waypoint?)  The pilot has to turn that option on in the various control files.
@ Bastien - I agree.
JJ Park to Everyone (10:54)
Lukas, Have you compared with AOA variables in slocum glider data and the AOA estimated by fitting your flight model?
Bastien Queste to Everyone (11:00)
Are flight models actually specific to gliders if you're regressing drag coefficients?
Bastien Queste to Everyone (11:01)
Lucas's model works great on Seaglider and on SeaExplorer
Anthony Bosse to Everyone (11:01)
indeed :) tried it on different platform too!
bit easier to optimize than Frajka Williams
JJ Park to Everyone (11:02)
Lucas’s model can be also used to target ballasting as well.
Soeren Thomsen  to Everyone (11:02)
You can let 4 gliders flow exactly the same path
Bastien Queste to Everyone (11:03)
I'm of the (potentially contentious) opinion that we should push one model that is well described and pushed for all gliders when doing RT processing. IMHO, I've found Lucas's to be very reliable.
Anthony Bosse to Everyone (11:03)
but if they have same path, they surely won't gave same angle of attack cause they have different geometry/drag
Soeren Thomsen  to Everyone (11:03)
it should be possible to state errors
JJ Park to Everyone (11:04)
It would be greatly helpful that someone can provide drag coefficients for several different settings and sensor installations.
Soeren Thomsen  to Everyone (11:06)
it is hard to hear you Anthony
Bastien Queste to Everyone (11:07)
Agreed, but from an SOP perspective, do we want multiple options or one recommended option?
It doesn't mean we shouldn't describe other models, and alternatives. On the contrary, we can rely on that to highlight strong and weak points.
Gerd Krahmann to Everyone (11:08)
can you get good DAC without measuring ? there won't be a proper flight model
Bastien Queste to Everyone (11:12)
and it has the benefit of also being able to diagnose poor drag parameters vs poor compass calibrations
Pierre Testor to Everyone (11:13)
We should talk about compass calibration. Impact in polar regions?
JJ Park to Everyone (11:15)
Good topic!!
Soeren Thomsen  to Everyone (11:16)
Thus it makes sense to list special issues related to different environments etc
Soeren Thomsen  to Everyone (11:16)
Tides, shallow water, deep water etc
Pierre Testor to Everyone (11:16)
+1
JJ Park to Everyone (11:16)
agree!
Bastien, do you know compass error after calibration in Arctic?
Bastien Queste to Everyone (11:21)
I've not done Arctic deployments, but I can fish out the Ross Sea data and get some numbers. This was early days 2009/2010 so it'd take a while to fish out ;)
Soeren Thomsen  to Everyone (11:23)
Yes please adapt just try to keep the deployment lifecycle idea please!
Soeren Thomsen  to Everyone (11:29)
I want to thank everyone. And I tried hard to get everyone on board working on these issues. If I missed someone please drag them in!
Pierre Testor to Everyone (11:30)
Sorry I have to leave. Nice discussions. Thanks a lot to everybody!
Soeren Thomsen  to Everyone (11:33)
Thanks to the leads!
And everyone joining!
Bastien Queste to Everyone (11:33)
Happy to write SeaExplorer bits as they're a little underrepresented
and otherwise, feel free to tag some bits for me to write.
Soeren Thomsen  to Everyone (11:36)
And leads please prepare a 3 min reporting for the linking session next week!
May 19 Wednesday 
	16:00 - 17:30 CEST / 7:00 - 8:30 PDT / 22:00 - 23:30  AWST
	Ocean Currents SOP: Reviewing of SOP (A. Pietri, A. Bosse., R. Todd)

Participants: Soeren Thomsen, Anthony Bosse, Robert Todd, Pierre Testor, François Bourrin, Nikolaos D. Zarokanellos , Alice Pietri, Lucas Merckelbach, Bastien Queste, JongJin Park, Yumi Song, Mathieu Gentil, Joe Gradone, Gerd Krahmann, Donglai Gong, Estelle Dumont, Gerasimi Anastasopoulou, Jake Steinberg, Louis Clement, Orens de Fommervault, Vincent Ma,  XXX add your name here please

Meeting notes: 

Alice: goes through the document, various people gave input during the week
Alice: include where/which sensors are attached and how they impact the flight of the glider
Alice: Anthony suggested that a description of different flight models / complexities / could be added, 
Alice: other platforms, specific missions/environment , contributions related to polar regions etc would be nice
Lucas: volunteers to describe the Slocum flight model, real time
Anthony: real time DACs are quite platform specific, in the DMQC we should conference to something which is not platform dependent 
Pierre: pre-deployment requirements: special spiral flights/ back and forth, 
Alice: U-turn
Pierre: refers to specific missions which can be done to improve DAC
Robert: compass calibration, average over longer time periods is needed, averaging period should be long, deep ocean is better, think of tides etc, short time scales are tricky
Alice: describe ideal mission for good DAC, constant depth, where to best place this
Jake: SeaGlider section, describe spirals, pitch and roll angles, run that mission to calibrate the compass, 
Robert: does this on land
Lucas: Slocum has something similar but has not tried it, externed program is needed, data has to be send to land, trust his compass calibration
Orens de Fommervault to Everyone (4:20 PM)
Helicoidal dive are also possible with the seaexplorer. Never try for compass calibration
Lucas: would not spend two days (glider in the water) to check the compass 
Robert: described on land compass calibration
Estelle: SeaGlider does the same in the water
Donglai: What kind of accuracy do you achieve for the angles? 
Robert: ~1 degree
Anthony: all gliders have different compass models, 
Robert: would love to know what the implications of a cheaper compass are, there seems to be a difference at least in the price
Estelle: not only compass accuracy, you also have the human error
Robert: refers to markers 
Estelle: Seagliders, have a lot of magnetic sources like batteries
Bastien: how to put the batteries might improve this
Robert: 
Estelle: What is available, also related to batteries in the field
Jake: two dives
Robert: 
Jake: deep gliders / batteries a bit different

Pierre: What about pitch validation?
Robert: They recorded it. Did not see a big difference. pitch and angle and attack are related, pitch and roll come from the same module
Lucas: pitch and role are not measured XXX (magnetically?), flew in shallow water with bottom track, the parts on the compass module (pitch, roll), module was leaking, computation and sensor did it wrong, put glider into a know angle
Bastien: refers to timestamp errors. please add details
Pierre: check that compass are not leaking
Lucas: if you have MicroRiders you measure twice which can help
Robert: not easy to align two instrument by 1º
Pierre: uncertainty first in º and later in cm/s
Donglai: asks, do you need to do before and after?
Robert: typically just before, due to practical reasons
Donglai: have you done onboard vs. delayed mode
Robert: they are close, 
Donglai: have you not seen cases where the ADCP is better than ?
Robert: no 

Robert: how does strong currents will affect the DAC
Soeren: you may want to dive deeper XXX. It may be important to state that measuring strong currents would be challenging
Robert: measuring DAC could event work better with strong current
Louis: XXX
Pierre: maybe not in the SOP, better in the DMQC paper
Soeren: maybe not everyone is aware of how to manage strong currents
Robert: I want to get rid of the opinion that gliders don’t work in strong currents
Donglai: it matters for how controllable the glider will be 
Robert: doesn’t fit in SOP
Soeren/Robert: discussion whether strong current etc should be discussed in an SOP
Donglai: strong shear?
Bastien (chat): Potential concerns when thinking about geostrophic velocity estimations if you want a clear transect? but agree doesn't affect DAC.
Gerd: in strong (extreme >1m/s over 20m) shear had to change the flight model 
Lucas: How could you tell?the glider cannot detect that
Gerd: used ship ADCP current profile and put that into the flight model as an estimated external force, worked. It is actually the inertia of the glider that creates an additional lift force for a pitched glider when it goes from one current to the next. This could be properly calculated instead of estimated and tuned.
Lucas: do we need to say something about transects of ADCP to referece shear profile
Robert: will be next SOP
Estelle: question related to compass calibration, (Soeren: did not understand the question)
Bastien Queste to Everyone (4:47 PM)
COMPASS_USE,4 and other derivatives are absolutely critical! 
Pierre: how do we account for magnetic deviations in the different models, polar regions
Robert: refers to work they did with spray, location depending processing, question is how important is the real time data
Pierre: shallow regions / shelf
Estelle: check before, real compass calibration in deep water, highly variable currents 
Robert: shallow dives, the glider is flying a larger fraction in a poor way, less an issue in deeper water, multiple cycles is not a big deal but challenging how to interpret, no constant flights/ depth etc are a challenge for interpretation
Pierre: what are scales / to perform multi-yo dives, tidal areas
Donglai: refers to deep water pump vs shallow pump, 
Lucas: has experience with shallow water, 40 m, 3 h time for being underwater, not ideal for tides, in the EEZ of Germany, comply with regulations, “gliders are a danger for ships”, has a paper how to get instantaneous currents with this, 
Robert: multicycle flights can help, surfacing is an issue, less surfacing
Pierre: pragmatic → what are the consequences of surfacing every yo in shallow environment 
Soeren: details/specificies for different science missions are fine
Donglai: 
Bastien: 

Lucas: post-processing depends on input data, Slocum deep pump can be an issue, if there are air bubbles in oil (not an issue for shallow glider, piston system)
Bastien: air bubble messed up everything
Bastien: flight model regression 
Gerd: air in the oil is not happening so much anymore in modern Slocums (the oilbladder material was changed around 2012), air compresses very quickly, says the effect is small during the whole dive, 
Lucas: refers to older missions, 2008?, 50 % buoyancy change
Gerd: fly full volumes
Bastien: weird and wonderful sensors, it is almost impossible to get out air bubbles out of these sensors
Estelle: refers to biofouling and drag change during the mission, quality of the DACs throughout the mission
Jake: SeaGlider newer flight model, which is updated during the mission with changing drag, Jim Bennett, new paper 2019 J-Tech http://hdl.handle.net/1773/44948 
Jake: are these parameters typically changes during a mission on other platforms
Gerd: refers to Slocum, possible to fit during the 
Gerd : flight model derived from Lucas with changeable drag coeff (cubic fit over time) where lots of biofouling (eg equator)
Jake: vehicle volume is changing during the mission, 
Gerd: 40g over a mission (weight is actually changing), water taken up by plastic ???
always getting heavier over the deployment...
Louis: can be corrected 
Bastien: 
Jake: flight model minimally affect cross track currents. Affect mostly along track currents
Estelle: GPS error
Robert: it is tiny
Estelle: should we advice a specific surfancing time
Robert: 
Estelle: shallow waters important

Ocean Currents DAC (SOP) https://docs.google.com/document/d/1nNtHyG0Lj3y1Le20EqFK9AmtKaUF6El_hAs5LHArSM8/edit 

