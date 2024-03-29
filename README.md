# appIDGameSpy

This is an unoptimized C++ console application that utilizes `vcpkg/curl` and `vcpkg/rapidjson` libraries for parcing appid's from appid.csv and bring some additional public information to .csv

## Usage

To use appIDGameSpy, follow these steps:

0. Download files from `/Shipped latest release/` dir.
1. Ensure you have `appid.csv` file in the root directory of the program.
2. The `appid.csv` file must contain Steam game appids, with one appid per line.
3. Ensure that there are no empty lines in the `appid.csv` file.
4. Run `RavenageGameSpy.exe`.
5. Wait for the program to finish running.
6. Check the output file in the `/result` directory. The filename will be `data_yyyy_mm_dd.csv`.

## Features

RavenageGameSpy has the following features:

- Avoidance of "429 Too Many Requests" errors using a wait timer for 30 seconds.
- Output data is saved in a CSV file with a filename that includes the current date.
- RavenageGameSpy is easy to use and provides a simple way to obtain data on multiple Steam games.

## Prerequisites for raw code

Before using raw code of appIDGameSpy, ensure that the following prerequisites are met:

- You have the `vcpkg` package manager installed on your system.
- You have installed the `curl` and `rapidjson` packages using `vcpkg` with x64-windows-static triplet.

## Alternative Sleep Functions

If you encounter issues with the `Sleep` function, you can try using one of the following alternative sleep functions:

- `std::this_thread::sleep_for` (C++11)
- `nanosleep` (POSIX)
- `SleepEx` (Windows)

These functions allow you to make the current thread sleep for a specified duration and are available on different platforms.
