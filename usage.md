# Docker setup
* Pull image
```
docker pull koanguyn0407/doom_arnold_deployed_code
```
* Run docker
```
docker run -ti --rm \
       -e DISPLAY=$DISPLAY \
       -v /tmp/.X11-unix:/tmp/.X11-unix \
        koanguyn0407/doom_arnold_deployed_code
```
* Activate environment
```
conda activate ml
```
# Pretrained models

## Defend the center / Health gathering

We provide a pretrained model for each of these scenarios. You can visualize them by running:

```bash
./run.sh defend_the_center
```

or

```bash
./run.sh health_gathering
```

# Visual Doom AI Competition 2017

We release the two agents submitted to the first and second tracks of the ViZDoom AI 2017 Competition. You can visualize them playing against the built-in bots using the following commands:

## Track 1 - Arnold vs 10 built-in AI bots
```bash
./run.sh track1 --n_bots 10
```

## Track 2 - Arnold vs 10 built-in AI bots - Map 2
```bash
./run.sh track2 --n_bots 10 --map_id 2
```

## Track 2 - 4 Arnold playing against each other - Map 3
```bash
./run.sh track2 --n_bots 0 --map_id 3 --n_agents 4
```

We also trained an agent on a single map, using a same weapon (the SuperShotgun). This agent is extremely difficult to beat.

## Shotgun - 4 Arnold playing against each other
```bash
./run.sh shotgun --n_bots 0 --n_agents 4
```

## Shotgun - 3 Arnold playing against each other + 1 human player (to play against the agent)
```bash
./run.sh shotgun --n_bots 0 --n_agents 3 --human_player 1
```