# Testing behaviour of Permission Set Groups
Particularly interested in removing PS from existing PSG
- Managed package upgrade
- Unlocked package (with/without namespace) upgrade
- Metadata API deployment
  
## Initial State
All packages at version 0.1 (and source package at equivalent commit) have PSGs with 3 permission sets (Custom Object, Custom App and Standard Object). Results after install (deploy):
- managed (04t08000000UK29AAG) - PSG created with 3 PSs
- unlocked (04t08000000UJztAAG) - PSG created with 3 PSs
- unlocked with nasmespace (04t08000000UK03AAG) - PSG created with 3 PSs
- source - PSG created with 3 PSs


## Test removal of PS
(Still cannot test Managed package - previous version was created without code coverage and cannot be promoted. Now limits for Develoepr org have been reached.)

All packages at version 0.2 (and source package at equivalent commit) has PSGs with 1 of the PSs removed. Upgrade (re-deploy shows)
- managed (04t08000000UK2EAAW) - PSG not updated, PS not removed
- unlocked (04t08000000UK0IAAW) - PSG updated and PS removed
- unlocked with nasmespace (04t08000000UK08AAG) - PSG not updated, PS not removed
- source - PSG updated and PS removed