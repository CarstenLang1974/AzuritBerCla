|STATE                     |description                                      |
| ------------------------ | ----------------------------------------------- |
|STATE_OFF          |off |
|STATE_REMOTE       |model remote control (R/C)|
|STATE_FORWARD      | drive forward |
|STATE_ROLL         | drive roll right/left |
|STATE_REVERSE      | drive reverse |
|STATE_CIRCLE       | drive circle |
|STATE_ERROR        | error |
|STATE_PERI_FIND    | perimeter find |
|STATE_PERI_TRACK   | perimeter track |
|STATE_PERI_ROLL    | perimeter roll |
|STATE_PERI_REV     | perimeter reverse |
| | |
|STATE_STATION          | in station |
|STATE_STATION_CHARGING | in station charging |
|STATE_STATION_CHECK    | checks if station is present |
|STATE_STATION_REV      | charge reverse |
|STATE_STATION_ROLL | charge roll |
|STATE_STATION_FORW | charge forward |
| | |
|STATE_MANUAL                 | manual navigation |
|STATE_ROLL_WAIT              | drive roll right/left |
|STATE_PERI_OUT_FORW          | outside perimeter forward driving |
|STATE_PERI_OUT_REV           | outside perimeter or stop on bumper : reverse driving (with mowing) |
|STATE_PERI_OUT_ROLL          | outside perimeter rolling driving  |
|STATE_PERI_OBSTACLE_REV      | perimeter reverse when hit obstacle |
|STATE_PERI_OBSTACLE_ROLL     | perimeter roll when hit obstacle |
|STATE_PERI_OBSTACLE_FORW     | perimeter forward after roll obstacle |
|STATE_PERI_OBSTACLE_AVOID    | perimeter circle to avoid obstacle |
|STATE_NEXT_LANE_FORW         | use after roll to reach the next lane |
|STATE_PERI_OUT_STOP          | use to stop slowly on perimeter before reverse |
|STATE_PERI_OUT_LANE_ROLL1    | roll always to 135 deg with brake |
|STATE_PERI_OUT_LANE_ROLL2    | roll one wheel to put in straight line with brake |
|STATE_PERI_OUT_ROLL_TOINSIDE | outside perimeter rolling driving |
|STATE_WAIT_AND_REPEAT        | use to repeat a state until something change for example find again perimeter by rolling |
|STATE_FORWARD_ODO            | drive forward odometry control straigh line and not speed in rpm |
| | |
| | |
STATE_TEST_COMPASS,    // drive roll right/left FOR A SPECIFIQUE ANGLE
STATE_PERI_OUT_ROLL_TOTRACK,   // outside perimeter rolling driving
STATE_PERI_STOP_TOTRACK, // brake when reach the wire before roll to start tracking
STATE_AUTO_CALIBRATE,  //wait until the drift is stopped and adapt the gyro and compass
STATE_ROLL_TO_FIND_YAW, //try to find the compass yaw = yawheading
STATE_TEST_MOTOR, //use to test the odometry motor
STATE_STOP_TO_FIND_YAW, // brake before roll to find yaw
STATE_STOP_ON_BUMPER,   //stop immediatly on bumper
STATE_STOP_CALIBRATE,   //don't move during 15 sec for DMP autocalibration.
STATE_SONAR_TRIG,      // when sonar detect obstacle brake gently before reverse
STATE_STOP_BEFORE_SPIRALE,     //brake gently before start the spirale
STATE_MOW_SPIRALE,      //mowing a CIRCLE ARC of increaseing diameter to make the spirale

STATE_ROTATE_RIGHT_360,  // simple mowing rotation at the beginning of the spirale
STATE_NEXT_SPIRE,  //go to next CIRCLE ARC in SPIRALE MODE
STATE_ESCAPE_LANE,  //grass is high need to reduce the lenght of the lane
STATE_PERI_STOP_TOROLL,  //use when timer start the mowing or when tracking and find RFID need to stop before roll
STATE_ROLL_TONEXTTAG,  //use when tracking and find RFID tag the mower roll to new heading
STATE_PERI_STOP_TO_NEWAREA,  //use when tracking and find RFID need to stop before roll to leave the area
STATE_ROLL1_TO_NEWAREA,  //use when tracking and find RFID need to roll to leave the area
STATE_DRIVE1_TO_NEWAREA,  //use when tracking and find RFID need to drive to leave the area
STATE_ROLL2_TO_NEWAREA,  //use when tracking and find RFID need to roll to leave the area
STATE_DRIVE2_TO_NEWAREA,  //use when tracking and find RFID need to drive to leave the area

STATE_WAIT_FOR_SIG2,  //use when the area 2 wait until sender send the signal
STATE_STOP_TO_NEWAREA,  //use to stop the mower in straight line after long distance moving with ODO and IMU
STATE_PERI_OUT_STOP_ROLL_TOTRACK, // after the mower rool to track we need to stop the right motor because it's reverse and the track is forward
STATE_PERI_STOP_TO_FAST_START,  // after the mower find a tag for find a new start entry point
STATE_CALIB_MOTOR_SPEED,  // we need to know how may ticks the motor can do in 1 ms to compute the maxododuration
STATE_ACCEL_FRWRD, // when start from calib or off need to accel before motorodo
STATE_ENDLANE_STOP //when mower is at the end of the lane avoid to reverse before roll
