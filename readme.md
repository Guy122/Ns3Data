Here i will show you my sql database that come from my simualtion that i build in NS3 on C++.

first step is to download the sql database from that link:
1.  Download the sql database from that link:
   ```
   https://drive.google.com/file/d/1Q_nTojYQzSMmUZViPwUioq39teKB__8R/view?usp=sharing
   ```
2.  You can use the LoadAndClean.ipynb to load the sql database and also search if there is worngs databases inside of it,
   beware that you need to uploud the database to your drive and monunt it to your colab notebook.

3. the sql database divide by names from the tamplate XuesYGnbsDateTime which X is number of Ues Y is the number of Gnbs and the DateTime is when the sql was been created.

4. all the simulations build in the following paramaters:
   ```
   bandwith of each gnb is 5mhz which mean that there is 26 RB's for each Gnb.
   Bandwith: 5MHZ.
   Moudulation: OFDMA
   Opertion: TDD
   Gnb's Transmition Power: 10dBm
   Services: UE_0 - NGMN_VOIP, UE_1 - Constant Packets Sizes others can be also NGMN_VIDEO,NGMN_FTP,NGMN_GAMING.
   see for more information https://www.nsnam.org/workshops/wns3-2022/17-bojovic-slides.pdf
   each gnb have maximum randomly 2-5 Ues attached.
   ```
   database tables:
   ```
   Gnbs:
   1. show Gnb's location,
   2. number pf ues attach and beam angle.
   UEs:
   1. show Ue's location, type of service
   2. Mcs_Dl and Mcs_Ul: show modulation code schmes (0 mean QPSK 22 mean 256 QAM)/
   3. RBs_Allocation_Dl and RBs_Allocation_Ul: show
   4. RSRP: 
   5. UE_Tx_Power:
   6. UlSINR_Per_RBs:
   7. harq_Dl and harq_Ul:
   8. tbs_Dl and tbs_Ul:
   9. ArrivalRateDl and ArrivalRateUl:
   ```

5. In lstm.ipynb I used the database to train lstm model that can predict the RBs Allocation. 
