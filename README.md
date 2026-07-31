the code is a lot of vibe code, i'm not familiar with this board platform, UAC2 and stuff... for now the code support 44->96khz for both 16 and 24 bit profile. i have tuned it to be precised because the board alone does not have much option for i2s frequency, i use pll3 (8 Mhz) for i2s. it still have some problem like pop when audio end...

the code is for CH32V307VCT6 development board (around 4.5$, quite cheap), pair with PCM5102. the wire config is:

- I2S2_WS (Word Select / LRCK): PB12
- I2S2_CK (Clock / SCLK): PB13
- I2S2_SD (Serial Data / SD): PB15

no MCLK since PCM5102 can use it own PLL to generate clock.
