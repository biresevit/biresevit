# Nenad Biresev

Senior Computer Vision Engineer in Bonn, Germany. I build perception systems that run on edge devices, and the cloud backends that schedule, monitor and update them.

Two of my own projects are public here.

## DrownShieldAI

Real-time drowning detection for swimming pools, running on an NVIDIA Jetson next to the pool. In trial deployment. [drownshieldai.com](https://drownshieldai.com/)

| Repository | What it is |
|---|---|
| [drowning-detection-portfolio](https://github.com/biresevit/drowning-detection-portfolio) | Detection and tracking, behaviour analysis, video action recognition, TensorRT export, experiment results. Python, PyTorch, TensorRT. |

## PokerFill

A platform that runs automated poker players on a fleet of PCs, controlled from the cloud. Five repositories, one per component. [pokerfill.com](https://pokerfill.com/)

```text
PokerBackoffice -> Azure SQL <- ScheduleController (Azure Functions)
                                     | commands / telemetry
                                PokerController
                                     | REST
                                  PDecision <- simulator
```

| Repository | Component |
|---|---|
| [PokerBackoffice](https://github.com/biresevit/PokerBackoffice) | Operations dashboard: schedules, live tables, hand replay, reporting, software updates for the PC fleet. JavaScript, Python, Azure Static Web Apps. |
| [ScheduleController](https://github.com/biresevit/ScheduleController) | Cloud scheduler: turns weekly targets into commands for the PCs. Python, Azure Functions, Azure SQL. |
| [PokerController](https://github.com/biresevit/PokerController) | Worker on each PC: connects to the poker platform and executes the scheduler's commands. Python, asyncio, WebSockets. |
| [PDecision-portfolio](https://github.com/biresevit/PDecision-portfolio) | Decision service: REST API that returns the action for a table state. C#, .NET 8, ASP.NET Core. |
| [simulator-portfolio](https://github.com/biresevit/simulator-portfolio) | Desktop table simulator used to test the decision service, with a demo video. C#, WPF. |
