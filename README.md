# University of Oregon Zero Waste Asset Cataloging

During my time working as the Administrative Assitant for the University of Oregon Zero Waste program, I was tasked as part of a program-wide initiative to modernize the way collection assets around campus are tracked in terms of location, quantity, type, and servicing. A component of this was integration of collection tracking into AiM, the university's asset management system. The university's Campus GIS program tracks spatial assets in AiM and in it's own database through the use of a 'RoomID'. This identification system is comprised of the building number followed by the room number for room-by-room asset tracking in every building. I integrated the RoomID identification system into the asset cataloging I did for the recylcing program in order to enable integration into the existing systems used by the university as well as added additional components to encode asset information into the RoomID to allow for comprehensive querying using just the RoomID.
<br/><br/>
Below is an example of an exterior asset RoomID. Every RoomID regardless of it's interior or exterior status begins with the building number. Since room numbers are not applicable for exterior assets, they are supplemented with the letter 'E' to denote an exterior asset followed by an asset identifier. Asset identifiers begin at 01 for a given building and each asset attached to that building has a unique identifier. A type identifier caps off the ID. A type chart can be referenced in Table 1 below.

![exterior](https://user-images.githubusercontent.com/76584053/159103103-cb2208cd-6a14-4617-813a-e27a37ab7e9d.png)
<br/><br/>

Below is an example of an interior asset ID. In order to take advantage of the full room-level asset tracking built into the Campus GIS system, the RoomID and ID are separated into two columns for the interior asset datasets. The RoomID convention follows the formula described above. The asset ID shown below 
begins with the room number, followed by a similar convention used for site identifiers for exterior assets. Instead, the identifier is prefixed with an 'I' to denote an interior asset followed by an site identifier. Similarly to exterior assets, identifiers begin at 01 for a given building but instead of each asset at a building having a distinct identifier, assets at the same site have like identifiers with each site having a unique identifier. A type identifier finishes the ID and can be referenced in Table 1 below.

![interior](https://user-images.githubusercontent.com/76584053/159105285-2e8c91f4-2c16-4dd2-a1f1-ed6d15386e7f.png)
<br/><br/>

Because the interior asset datasets span multiple floors, representing them with static maps here would be clunky to say the least. The interior asset data can be viewed by downloading 'interior_assets.gpkg' 
