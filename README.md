# OCR Word Search Solver

This project is a word-search puzzle solver developed in C by a team of four EPITA students.

The goal is to solve word-search puzzles from an image using Optical Character Recognition (OCR). The program processes the image, identifies the letters and words, and searches for them in the grid.

## Features

- Image loading through a graphical interface
- Automatic and manual image rotation
- Image preprocessing and noise reduction
- Detection and extraction of the grid and word list
- Letter recognition using a neural network
- Word searching in all 8 directions
- Display of the solved puzzle

## How It Works

The program follows several steps:

1. **Image processing:** The image is loaded, straightened and cleaned.
2. **Extraction:** The grid and word list are detected and separated into individual letters.
3. **OCR:** A neural network recognizes the letters.
4. **Solving:** The program searches for each word horizontally, vertically and diagonally.
5. **Results:** The detected words are highlighted on the solved grid.

## Technologies

- **C** for the application and algorithms
- **GTK+3** for the graphical interface
- **SDL2 / SDL2_image** for image processing
- **Neural network** for character recognition

## Compilation and Usage

The project was developed for Linux and requires GCC, Make, GTK+3, SDL2 and SDL2_image.

Clone the repository:

```bash
git clone https://github.com/Aliya-prc/Project_Ocr.git
cd Project_Ocr/Projet_Ocr
```

Compile and launch the application:

```bash
make
./projet_ocr
```

Once the application is running:

1. Click **Open Image** to load a puzzle.
2. Use **Auto-Rotate** or the manual controls to adjust the image.
3. Use **Denoise** if necessary.
4. Click **Solve Grid** to process the image.

Recognition accuracy depends on the quality of the input image.

## Project Structure

The main source code is organized into several modules:

- `src/autorotation/`: automatic image alignment and rotation
- `src/extraction/`: image preprocessing and letter extraction
- `src/ocr/`: character recognition
- `src/solver/`: word-search solving algorithm
- `src/gui/`: graphical interface
- `src/result/`: display of the results

## My Contribution

My main contribution was the **automatic image rotation module**.

I worked on detecting image inclination through edge analysis and correcting its orientation using image rotation and interpolation.

This preprocessing step helps improve image alignment before grid extraction and character recognition.

## About the Project

This project gave our team practical experience in image processing, OCR, algorithms and integrating multiple C modules into one application.

It also involved coordinating our work and combining the different parts of the application into a complete processing pipeline.
