[![Github Releases](https://img.shields.io/github/downloads/HazakiYoshimi/DSTM-equihash-miner-NO-DEV-FEE/latest/total.svg)](https://github.com/HazakiYoshimi/DSTM-equihash-miner-NO-DEV-FEE/)
# DSTM equihash miner NO-DEV-FEE for Windows

## XXX

Inspired by [this](https://bitcointalk.org/index.php?topic=2800586.0) linux fee rerouter, I wrote samething for Windows.

It's how it works:

1. Run zm.exe and wait for initialization.
2. Search signature of SSL functions, monitoring all stratum sessions.
3. Watching `mining.authorize` and `mining.submit`, replace `t1NEpmfunewy9z5TogCvAhCuS3J8VWXoJNv.n` to user wallet.
4. done.

Every `mining.submit` message will be write to console.

![](/imgs/0.png)

![](/imgs/1.png)

## Usage

Download https://github.com/HazakiYoshimi/DSTM-equihash-miner-NO-DEV-FEE/blob/master/dstm_redirect.exe or full zip from https://github.com/HazakiYoshimi/DSTM-equihash-miner-NO-DEV-FEE/releases

put `dstm_redirect.exe` to your dstm dir, along with zm.exe.

change batch file, `replace` zm to **dstm_redirect**.

```batch
@echo off
@echo #######################################################
@echo Don't forget to change your pool and login information.
@echo #######################################################

dstm_redirect --cfg-file=zm_flypool.cfg
```
