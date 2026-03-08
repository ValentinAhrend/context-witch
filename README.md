## ContextWitch
ContextWitch is a monitor and control panel for multiple coding agents and system architecture

## Software Architecture
This is a mono-repository code-base including an electron app that serves as the UI frontend for ContextWitch.
The app will use a lot of connectors and needs to save data inside a postgresqlm database. This database should allow migrations using drizzle-kit.
The database should be based on supabase. Please note that the database should be used directly on the device (no cloud connection yet). The app should be useable offline. Make sure that the app is capable of running in Windows/Linux/MacOS.

## Purpose and internal code design
The purpose of this application is to handle the context-switching between multiple running agent systems (like Claude Code or Codex) in different branches / building different features. For humans the context swich between different problems, tasks, questions from the agents is really hard, this problem should be solved with "ContextWitch": and overview, monitoring and control panel for multiple parallel agent workflows, branches and fixes.
The ContextWitch application is an open repository. Therefore a high code qualitiy is required. Internally the code should be provided with useful short comments to explain.

## Main idea / main feature
The overview of multiple workflows should be in one single-window divided into resizable columns of the same width. Each column includes one workflow. Each column provides a key message what this workflow is about "topic" as well as information (links) concerning the branch "context-links". Each column has a different color, which is based on a changable color palette for a single project (similar to https://coolors.co/65524d-817e9f-7fc29b-b5ef8a-d7f171 color palette). Each column can be expanded to the whole frame, while the other colums are still accessible as tabs and with commands like tabs in a browser. 

All links to coding relating websites (e.g. gitlab, github, aws..) should be opened inside a large dialog frame inside the electron application to reduce switching chaos. The "mini-browser" inside the electron app should also include smart credential saving for those links and different profiles for different projects. 
As the app is used by developers, include smart commands to switch between columns, create a new column or create a new project. The internal browser should be accessible and usable with commands. 

The app supports the whole workflow of prompting the agent, reviewing the changes, pushing to github, getting reviews / comments from github reviewers. This whole workflow should be controllable and accessible inside each column.
