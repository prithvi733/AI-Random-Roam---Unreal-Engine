# AI-Random-Roam---Unreal-Engine
# Aim:
To implement an AI character in Unreal Engine that roams randomly within a defined area using Behavior Trees and Navigation Mesh.
# Procedure:
1.Navigation Setup
.Add a NavMeshBoundsVolume to your level and scale it to cover the roamable area.
.Ensure navigation is built (press P to visualize the navmesh).

2.Create AI Character
.Create a new Character or Pawn Blueprint (e.g., BP_AICharacter).
.Add an AIController Blueprint (e.g., BP_AIController) and assign it to your AI character.

3.Set Up Behavior Tree
.Create a Behavior Tree (e.g., BT_RandomRoam) and a corresponding Blackboard.
.Add a Blackboard Key (e.g., TargetLocation) of type Vector.

4.Implement Roaming Logic
.In the Behavior Tree, use the following structure:
.Root ➝ Selector
.Sequence
.Find Random Location (custom task to set TargetLocation)
.Move To node (uses TargetLocation)
.Create a custom BTTask Blueprint for finding a random location using UNavigationSystemV1::GetRandomPointInNavigableRadius.

5.Place and Test
.Place your AI character in the level.
.Assign the AI Controller and Behavior Tree.
.Play the scene and observe the AI roaming randomly.

# Output:

![image](https://github.com/user-attachments/assets/432d7ace-1dd8-4e8b-b214-4ff9500c5f0c)

![image](https://github.com/user-attachments/assets/1a94daf8-cb62-438f-8732-4f97da992cec)

![image](https://github.com/user-attachments/assets/15d1873f-bf3f-449b-8d12-451771984976)

![image](https://github.com/user-attachments/assets/5c385a79-a465-4fe7-b229-304f1d20e639)

![image](https://github.com/user-attachments/assets/be6c1d61-3d64-4f20-9ce3-129b364f51ee)

# Result:
The AI character successfully roams within the defined NavMesh area, choosing random destinations at intervals using the Behavior Tree logic.




