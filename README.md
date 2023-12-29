# Proof of Concept for a Turn Based City Builder
> Hello! <br>
> This is the exectuable of a Turn Based City Builder project that I worked on recently. <br> <br>
> This project is a proof of concept, it does not contain a full gameplay loop. Instead this was an exploration of the different systems that go into creating a grid based, turn based, city builder game would require. <br> <br>
> Check out the game if you want to! Otherwise this README is going to go through each system that was implemented for this project <br>

![Overarching Gif](GithubImages/OverArchingGif.gif)

<br>

## Table of Contents
- [Exploration and Tile Generation](#Exploration-and-Tile-Generation)
- [Turn System](#Turn-System)
- [Build System](#Build-System)
- [Movement](#Movement)
- [Potential Routes for Further Development](#Potential-Routes-for-Further-Development)

<br>

| Farm | Village | Hamlet |
|---|---|---|
| ![Farm](GithubImages/Farm.gif) | ![Village](GithubImages/Village.gif) | ![Hamlet](GithubImages/Hamlet.gif) |

## Exploration and Tile Generation

> When the game is first launched the player is placed on a 3x3 grid of tiles. <br>
> The player can click on the search tiles around the edge of the grid in order to generate an additional tile on the grid.<br> 
<br>
![ExploreGif](GithubImages/ExploreGif.gif)
<br>

> In the backend, there is a modifiable ruleset about which tiles can be generated next to each tile. This allows a designer to change how the terrain generation feels with just a simple alteration to the tile ruleset. This also allows for interesting specialized generation depending on the tiles surrounding environment<br>
> For example if a user explores next to an ocean tile that tile can only become a water, beach, or grasslands tile. <br>

<br>

![WaterTile](GithubImages/WaterTile.gif)
<br>

> When the search tile is touching two or more already explored tiles, the game instead chooses the intersection of the terrain types available of the surrounding tiles. This can cause a problem if there are no available terrain in the intersection of the terrains, so to avoid this, all terrains must have a grasslands terrain in their possible explore terrains. <br>
> This avoids the situation of the intersection between two different terrain types to be zero. 
<br>


## Turn System

> This project works on a turn based system. The system is relatively simple, the player is given three actions per turn. The player can perform two different types of actions. They can either explore and generate new tiles or they can build buildings on the previously generated tiles. When they have used all three actions they will not be able perform another action until after they end their turn.<br>
> They must perform all three actions in order to end their turn <br>
<br>
![TurnManagement](GithubImages/TurnManagement.gif)
<br>
> When the player ends their turn the year in the top right updates as well as all four resources. Each resource has symbol next to it that informs the player whether that resource will increase, decrease, or stay the same. <br>
> Currently the top three resources do not have functionality however the bottom resource can stop a player from creating new buildings.

## Build System

> Uh Yeah

## Movement

## Potential Routes for Further Development

> Uh