# 🌊 sar-flood-segmentation - Spot Floods From Space Easily

[![Download sar-flood-segmentation](https://img.shields.io/badge/Download-sar--flood--segmentation-brightgreen?style=for-the-badge&logo=github)](https://github.com/hyfreughurhgufrhbg/sar-flood-segmentation)

A research tool that compares different artificial intelligence models to see which one maps flooded areas most accurately from satellite radar images. Built as an MSc dissertation project at the University of Hull, it tests how well these models perform across different parts of the world.

## 📥 Download the Application

Visit this link to download the application:

**https://github.com/hyfreughurhgufrhbg/sar-flood-segmentation**

Save the downloaded folder somewhere easy to find, such as your Desktop or your Documents folder.

## 🚀 Getting Started

This guide is written for anyone, even if you have never used a research tool or written a single line of code. You do not need to understand radar imagery, neural networks, or satellite orbits to get started. You only need to follow the steps in order.

The application is a collection of files that work together. When you download it, you receive everything needed to run the flood mapping experiments on your own Windows computer. Think of it as a recipe book: the files contain the instructions, and your computer does the cooking.

Before you begin, make sure your downloaded folder is unzipped and sits in a simple location. Avoid deeply nested folders like `C:\Users\Name\Documents\Projects\2024\Research\Final\Copy\sar-flood-segmentation`. A path such as `C:\sar-flood-segmentation` is much easier for both you and the software to handle.

## ✅ What You Need Before You Start

A Windows 10 or Windows 11 computer with:

- At least 8 GB of memory (16 GB is comfortable)
- Around 10 GB of free disk space for the project files and sample data
- A stable internet connection for the initial download
- A screen resolution of 1280×720 or higher

No graphics card is required. The application will run on a standard laptop, though it will take longer on older machines. If your computer was made in the last five years, you are almost certainly fine.

## 🖥️ Running the Application Step by Step

Step 1. Open your web browser and go to the download link shown at the top of this page.

Step 2. On that page, use the download control to save the application files to your computer.

Step 3. When the download finishes, locate the saved folder. Windows usually places downloads in your `Downloads` folder unless you chose a different destination.

Step 4. If the folder is compressed, right-click it and choose Extract All. Accept the suggested location and wait for the extraction to complete. You should now see a normal folder containing several files and subfolders.

Step 5. Move that folder to a short, simple path such as `C:\sar-flood-segmentation`.

Step 6. Open the folder and look for the main launch file included in the project. Double-click it to start the application. A black text window may open first; this is normal and shows progress messages as the software starts up.

Step 7. Wait. The very first launch takes the longest because the software prepares itself. Give it several minutes on a slower computer and resist the urge to close the window.

Step 8. Once preparation finishes, the application is ready to use. Keep the window open while you work.

## 🧭 How To Use It

The application follows a simple pattern: you choose a set of satellite images, you choose one or more models to test, and you press start. The software then produces maps showing which areas it believes are flooded.

A typical session looks like this:

1. Select the folder containing the Sentinel-1 radar scenes you want to analyse.
2. Choose one model or several models to compare.
3. Set how long the software should train or how many samples to process.
4. Start the run and watch the progress messages.
5. When it finishes, open the results folder to see the flood maps and the accuracy scores.

The accuracy scores are the heart of the project. Each number tells you how closely the model's flood map matched the correct human-made answer. Higher is better. Comparing these numbers across models and across regions is exactly what this project was designed to do.

## 🔍 What It Does

Flood mapping from space is difficult. Clouds block ordinary cameras, and floods often happen during the very storms that bring the clouds. Radar satellites solve this because radar sees through cloud cover and works day or night. The catch is that radar images look nothing like photographs. They are grainy, speckled, and hard for a human to read quickly.

This project trains computer models to read those radar images and pick out water. It then compares two families of models:

- **Convolutional models** such as U-Net, which have been the standard approach for years
- **Transformer models** such as SegFormer, which are newer and better at understanding the wider context of a scene

By running both on the same data, the project answers a practical question: is the newer approach actually worth it for flood mapping, and does it hold up when you move from one part of the world to another? That last point matters enormously. A model trained on floods in one country can quietly fail when applied to a different continent with different terrain, different rivers, and different building styles.

## 🧩 Understanding the Models

You do not need to know the mathematics, but a short explanation helps you interpret the results.

**U-Net** works like a careful inspector with a magnifying glass. It looks at small patches of the image, then gradually zooms out to build a complete picture. It is fast, reliable, and well understood.

**SegFormer** works more like a reader skimming a page. It considers distant parts of the image at the same time, which helps it recognise that a stretch of dark pixels near a river is probably water rather than shadow.

Neither model is automatically correct. Each makes different mistakes. The comparison is what gives the project its value.

## 📊 About the Data

The project uses Sen1Floods11, a well-known public collection of Sentinel-1 radar scenes paired with hand-labelled flood maps. The collection covers flood events across multiple continents, which is what makes cross-geographic testing possible.

Data is organised into training scenes and test scenes. The software learns from the training scenes and is then judged on the test scenes it has never seen. This is the fair way to measure performance, and it is the standard approach in the field.

## 🛠️ Common Problems and Fixes

**The window closes immediately.** This usually means the folder was moved after the software started, or the path contains unusual characters. Move the folder to `C:\sar-flood-segmentation` and try again.

**The software says a file is missing.** The download may have been interrupted. Delete the folder and download it again from the link above.

**Everything is very slow.** Close other programs. Large image files consume a lot of memory, and a busy computer will crawl.

**Windows shows a security prompt.** Choose the option that allows the file to run. Research tools downloaded from the internet often trigger these prompts because Windows does not recognise them yet.

**The text window shows red warnings.** Warnings are usually harmless progress notes. Only stop if the window closes or the software asks you for input.

## 💡 Tips for Best Results

Start with a small number of images rather than the full collection. This lets you confirm everything works before committing hours of computer time.

Keep a notebook of what you ran and what scores you saw. Comparing results is far easier when you have written them down.

Do not change several settings at once. Change one thing, run the test, and note the difference. This is how real research is done.

Let long runs finish overnight. Radar image processing is heavy work, and a quiet computer completes it much faster.

## 🙋 Frequently Asked Questions

**Do I need an internet connection to use it?** Only for the initial download. After that, everything runs locally on your computer.

**Can I use my own satellite images?** Yes, provided they are Sentinel-1 radar scenes in a compatible format. The included data is there to help you learn the workflow first.

**Is this a finished product?** It is a research project from a master's dissertation. It is stable and documented, but it is built for experimentation rather than commercial deployment.

**Can I run it on a Mac or Linux machine?** The instructions here focus on Windows. The underlying tools are cross-platform, but Windows is the supported path for this guide.

**Who is this for?** Students, researchers, and curious newcomers who want to see how modern AI handles real flood mapping problems.

## 📄 Credits

Developed as an MSc dissertation at the University of Hull. Built on open-source tools for deep learning and remote sensing, and on the publicly available Sen1Floods11 dataset. Thanks to the researchers who make both the data and the software freely available.

Keywords: deep-learning, flood-mapping, pytorch, remote-sensing, sar, segformer, semantic-segmentation, sen1floods11, sentinel-1, unet