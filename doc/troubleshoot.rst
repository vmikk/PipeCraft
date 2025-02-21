.. image:: _static/PipeCraft2_icon_v2.png
  :width: 100
  :alt: logo

.. |learnErrors| image:: _static/troubleshoot/learnErrors.png
  :width: 250
  :alt: Alternative text

.. |dimnames| image:: _static/troubleshoot/dimnames.png
  :width: 250
  :alt: Alternative text
  
|

================
Troubleshooting
================

This page is developing based on user feedback.

____________________________________________________

ASVs workflow
==============

.. error::

 "Error in derepFastq(fls[[i]], qualityType = qualityType) : Not all provided files exist. Calls: learnErrors -> derepFastq. Execution halted"

|learnErrors| 

**Possible reason**: Some samples have completely discarded by quality filtering process. 

**Fix**: Edit the quality filtering settings or excluded poor quality samples prior ASVs workflow. 

____________________________________________________

.. error::

 "Error in dimnames(x) <- dn : length of 'dimnames' [2] not equal to array extent"

|dimnames|

**Possible reason**: Using only one or two samples to generate ASVs table.

**Fix**: Include at least three samples to ASVs workflow to generate ASVs table. Note: fixing this error in the upcoming releases. 

General
=======

.. error::

 Conflict. The container name XXX is already in use by container "XXX".
 You have to remove (or rename) that container to be able to reuse that name.

**Reason**: Process stopped unexpectedly and docker container was not closed.

**Fix**: Remove the docker container (not image!) that is causing the conflict
