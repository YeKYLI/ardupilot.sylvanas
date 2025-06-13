# debug

./waf configure --board sitl --debug && ./waf copter

sim_vehicle.py -v copter

## first instruction

HAL_Empty::run

# 业务

## 悬停

## 起飞

## 航点

## 避障

### 时刻处理mavlink消息 将避障信息存储在数据库中

AP_Proximity 

GCS_MAVLINK::handle_obstacle_distance

AP_Proximity::handle_msg

AP_Proximity_Backend::handle_msg

AP_Proximity_MAV::handle_obstacle_distance_msg  ｜ 将传感器原始数据转化为飞控模型可理解的环境信息

### 在运行过程中调用避障算法再执行避障

AC_Avoidance 

SCHED_TASK(avoidance_adsb_update, 10, 100, 138)  ｜  作为一个定时任务执行的

Copter::avoidance_adsb_update

AP_Avoidance::update()

# Module

## schduler

# Library

## Motor

电机控制

## Test

tests/*

gtest

## Benchmark

benchmarks/*

gbenchmark

## Bootloader

### sitl