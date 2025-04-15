NS3 5G Simulation Database & LSTM Prediction

This repository contains a simulation-based SQL database generated using NS3 (C++) and a predictive model built with LSTM to forecast Resource Block (RB) Allocation in a 5G wireless environment.
📥 Download the Database

You can download the SQL database from the following link:

https://drive.google.com/file/d/1Q_nTojYQzSMmUZViPwUioq39teKB__8R/view?usp=sharing

🛠️ Getting Started

    Upload the SQL file to your Google Drive.

    Open LoadAndClean.ipynb in Google Colab.

    Mount your Drive and load the database.

    Use the notebook to clean and verify the data (e.g., check for corrupted entries).

🗃️ Database Structure

The database files are named using the format:
XuesYgnbsDateTime
Where:

    X = Number of UEs

    Y = Number of gNBs

    DateTime = Timestamp of creation

📌 Simulation Parameters

    Bandwidth per gNB: 5 MHz → 26 RBs

    Modulation: OFDMA

    Operation Mode: TDD

    gNB Power: 10 dBm

    Services Used:

        UE_0 → NGMN_VOIP

        UE_1 → Constant Packet Sizes

        Others may include: NGMN_VIDEO, NGMN_FTP, NGMN_GAMING

    Each gNB: Randomly connected to 2–5 UEs

More details available in the NS-3 Workshop Slides
📋 Tables Overview

Gnbs Table

    gNB location

    Number of connected UEs

    Beam angle

UEs Table

    UE location & service type

    Mcs_Dl, Mcs_Ul (modulation schemes)

    RBs_Allocation_Dl, RBs_Allocation_Ul

    RSRP, UE_Tx_Power, UlSINR_Per_RBs

    harq_Dl, harq_Ul, tbs_Dl, tbs_Ul

    ArrivalRateDl, ArrivalRateUl

🤖 Predictive Model

The lstm.ipynb notebook contains an LSTM-based model trained on the SQL data to predict future RB allocations.
