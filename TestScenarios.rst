==============
Test Scenarios
==============

V textovej forme kvôli problémom s podporou vo verziách Visual Paradigm a 
nedostatku času.


---------------------
Dependency assignment
---------------------

^^^^
Main
^^^^

* **Super use case:** Dependency assignment
* **Brief description:** Asset owner assigns a dependency for an asset.
* **Preconditions:** The asset owner is logged in.
* **Postconditions:** The dependency was succesfully assigned.

===== ==================================== =====================================
Event Actor input                          System Response
===== ==================================== =====================================
1.    Asset owner clicks the 
      "dependencies" tab button.
2.                                         The system opens the "dependencies"
                                           tab, displaying a list of 
                                           dependencies with their completion 
                                           stages.
3.    Asset owner clicks the 
      "Add dependencies" button.
4.                                         The system shows a list of assets
                                           with a filter bar at the top.
5.    Asset owner selects the assets to 
      add as dependencies.
6.                                         The system checks the assets for any
                                           circular dependencies, and if any of
                                           the assets is in a higher or 
                                           branching milestone compared to the 
                                           depending asset. It also checks if
                                           any of the assets is already a 
                                           dependency of the depended asset.
7.                                         The system determines that there are
                                           no circular dependencies or 
                                           milestone conflicts.
                                           No visual output is displayed.
8.    Asset owner clicks the "Ok" button.
9.                                         The system adds the dependencies and
                                           returns the user to the 
                                           "dependencies" tab, with updated 
                                           contents.
===== ==================================== =====================================


^^^^^^^^^^^^^
Alternative 1
^^^^^^^^^^^^^

* **Super use case:** Dependency assignment
* **Brief description:** Asset owner tries to assign an existing dependency.
* **Preconditions:** The asset owner is logged in.
* **Postconditions:** The dependency was succesfully assigned.

===== ==================================== =====================================
Event Actor input                          System Response
===== ==================================== =====================================
1.    Asset owner clicks the 
      "dependencies" tab button.
2.                                         The system opens the "dependencies"
                                           tab, displaying a list of 
                                           dependencies with their completion 
                                           stages.
3.    Asset owner clicks the 
      "Add dependencies" button.
4.                                         The system shows a list of assets
                                           with a filter bar at the top.
5.    Asset owner selects the assets to 
      add as dependencies.
6.                                         The system checks the assets for any
                                           circular dependencies, and if any of
                                           the assets is in a higher or 
                                           branching milestone compared to the 
                                           depending asset. It also checks if
                                           any of the assets is already a 
                                           dependency of the depended asset.
7.                                         The system determines that one or
                                           more of the selected assets is 
                                           already a dependency of the depended
                                           asset.
8                                          The system visually marks all 
                                           conflicting assets.
9.    Asset owner corrects the selection.
10.                                        The system adds the dependencies and
                                           returns the user to the 
                                           "dependencies" tab, with updated 
                                           contents.
===== ==================================== =====================================


^^^^^^^^^^^^^
Alternative 2
^^^^^^^^^^^^^

* **Super use case:** Dependency assignment
* **Brief description:** Asset owner aborts the depency assignment dialog.
* **Preconditions:** The asset owner is logged in.
* **Postconditions:** The asset owner is on the depency tab, dependencies did not change.


===== ==================================== =====================================
Event Actor input                          System Response
===== ==================================== =====================================
1.    Asset owner clicks the 
      "dependencies" tab button.
2.                                         The system opens the "dependencies"
                                           tab, displaying a list of 
                                           dependencies with their completion 
                                           stages.
3.    Asset owner clicks the 
      "Add dependencies" button.
4.                                         The system shows a list of assets
                                           with a filter bar at the top.
5.    Asset owner selects the assets to 
      add as dependencies.
6.                                         The system checks the assets for any
                                           circular dependencies, and if any of
                                           the assets is in a higher or 
                                           branching milestone compared to the 
                                           depending asset.
7.                                         The system determines that there is
                                           either a circular dependency, a
                                           milestone mismatch or an already 
                                           assigned dependency.
8                                          The system visually marks all 
                                           conflicting assets.
9.    Asset owner finds no way to resolve
      the conflict, clicks the "Cancel"
      button.
10.                                        The system returns the user to the 
                                           "dependencies" tab. Dependencies 
                                           are left unchanged.
===== ==================================== =====================================

------------------------
Asset storage & transfer
------------------------
