# Customize PS1

Provide bash file to custom PS1.

## Prerequisite

`systemd-detect-virt` is required to get virtual environment

## How to use

1. Get the file `.bash_customize_ps1` on your host and source it in your bashrc
   file:

  ```bash
  source $HOME/.bash_customize_ps1
  ```

2. Call the function `custom_ps1` with corresponding colors

  ```bash
  USER_COLOR=blue
  MACHINE_COLOR=blue
  WORKSPACE_COLOR=green
  TIME_COLOR=yellow
  SEPARATOR_COLOR=white
  
  custom_ps1 $PRIMARY_COLOR $WORKSPACE_COLOR $TIME_COLOR $SEPARATOR_COLOR
  ```

## List of colors

|display|Xterm Number|Name|
|:-----:|:-----------|:---|
|![#3a3a3a](https://placehold.co/15x15/3a3a3a/3a3a3a)|237|black|
|![#800000](https://placehold.co/15x15/800000/800000)|1|red|
|![#5f875f](https://placehold.co/15x15/5f875f/5f875f)|65|green|
|![#afaf00](https://placehold.co/15x15/afaf00/afaf00)|142|yellow|
|![#005f87](https://placehold.co/15x15/005f87/005f87)|24|blue|
|![#875faf](https://placehold.co/15x15/875faf/875faf)|97|magenta|
|![#87afd7](https://placehold.co/15x15/87afd7/87afd7)|110|cyan|
|![#c6c6c6](https://placehold.co/15x15/c6c6c6/c6c6c6)|251|white|
|![#ff87d7](https://placehold.co/15x15/ff87d7/ff87d7)|212|pink|
|![#ff875f](https://placehold.co/15x15/ff875f/ff875f)|209|orange|
|![#af875f](https://placehold.co/15x15/af875f/af875f)|137|brown|
|![#949494](https://placehold.co/15x15/949494/949494)|246|grey|

## List of functions

* `custom_ps1` fontground color for your PS1 with separators

  ```bash
  source "${HOME]/.bash_customize_ps1"
  custom_ps1 yellow yellow blue magenta white
  ```

  ![Custom ps1 example](./img/custom_ps1-example.png)
* `custom_ps1_bg` background color for your PS1 with arrows shape

  ```bash
  source "${HOME]/.bash_customize_ps1"
  custom_ps1_bg brown red black white
  ```

  ![Custom ps1 bg example](./img/custom_ps1_bg-example.png)

