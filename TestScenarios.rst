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
* **Preconditions:** Asset owner is logged in, at an asset page.
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
* **Preconditions:** Asset owner is logged in, at an asset page.
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
8.                                         The system visually marks all 
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
* **Preconditions:** Asset owner is logged in, at an asset page.
* **Postconditions:** Asset owner is on the depency tab, dependencies did not change.


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
8.                                         The system visually marks all 
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

^^^^
Main
^^^^

* **Super use case:** Asset storage and transfer.
* **Brief description:** Asset creator uploads an asset file.
* **Preconditions:** Asset creator is logged in, at an asset page.
* **Postconditions:** The asset file was succesfully uploaded.

===== ==================================== =====================================
Event Actor input                          System Response
===== ==================================== =====================================
1.    Asset creator clicks the 
      "upload file" button.
2.                                         The system verifies if the asset
                                           creator has a permission to upload 
                                           for this asset.
3.                                         The system determines that the 
                                           asset creator can be allowed to 
                                           upload the file.
4.                                         The system opens the "select file"
                                           dialog, allowing the user to select 
                                           a file to upload.
5.    Asset creator selects the file.
6.                                         The system begins uploading the file.
7.                                         The upload successfully completes.
8.                                         The system verifies the file type,
                                           and any limits set by asset owner 
                                           (e.g. file size, texture resolution, 
                                           triangle count)
9.                                         The system accepts the uploaded file 
                                           and replaces the current (if any)
                                           asset file with it.
10.                                        The system updates the asset page.
===== ==================================== =====================================


^^^^^^^^^^^^^
Alternative 1
^^^^^^^^^^^^^

* **Super use case:** Asset storage and transfer.
* **Brief description:** Asset creator does not have a permission to upload an asset file.
* **Preconditions:** Asset creator is logged in, at an asset page.
* **Postconditions:** Asset file is left unchanged.

===== ==================================== =====================================
Event Actor input                          System Response
===== ==================================== =====================================
1.    Asset creator clicks the 
      "upload file" button.
2.                                         The system verifies if the asset
                                           creator has a permission to upload 
                                           for this asset.
3.                                         The system determines that the 
                                           asset creator can't upload the file.
                                           upload the file.
4.                                         The system shows a message informing
                                           the asset creator that they can't
                                           upload the file
===== ==================================== =====================================


^^^^^^^^^^^^^
Alternative 2
^^^^^^^^^^^^^

* **Super use case:** Asset storage and transfer.
* **Brief description:** Asset upload fails.
* **Preconditions:** Asset creator is logged in, at an asset page.
* **Postconditions:** Asset file is left unchanged.

===== ==================================== =====================================
Event Actor input                          System Response
===== ==================================== =====================================
1.    Asset creator clicks the 
      "upload file" button.
2.                                         The system verifies if the asset
                                           creator has a permission to upload 
                                           for this asset.
3.                                         The system determines that the 
                                           asset creator can't upload the file.
                                           upload the file.
4.                                         The system shows a popup informing
                                           the asset creator that they can't
                                           upload the file
3.                                         The system determines that the 
                                           asset creator can be allowed to 
                                           upload the file.
4.                                         The system opens the "select file"
                                           dialog, allowing the user to select 
                                           a file to upload.
5.    Asset creator selects the file.
6.                                         The system begins uploading the file.
7.                                         The upload fails before completing.
                                           The system shows a message informing
                                           the user about the failed upload,
===== ==================================== =====================================
