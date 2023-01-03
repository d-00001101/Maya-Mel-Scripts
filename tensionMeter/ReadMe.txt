// Copyright (C) 2002 Daniel Arzabe

// For changes or additions you can contact me at: darzabe@gmail.com

// 

//  tensionMeter.mel

//
//  This script was written to add a contraction effect to my characters underlying
//  muscle structure.  The flexing of the muscle was dependent on the speed of a joints
//  rotation with the option to explicitly control the flexing.
//
//
//
//   <installation> just copy scripts to one of your directories in your Maya script path.
//                  I've also included two bmp icons if you decide to make shelf buttons.
//
//
//

//   <description>  This script calculates the magnitude of a keyable attribute's change in value 

//                  to "drive" a secondary value.

//

//   <synopsis>   tensionMeterProc( int $createAddGroup, string $driverAttr, string $drivenAttr, string $newAttrName, string $groupName)

//

//   <arguments>   int $createAddGroup - 0 will create a new tensionMeter group

//                                       1 will add a user defined attribute to an existing tensionMeter group

//                 string $driverAttr - the name of the "driver" node and the attribute - ex. ball.rotateX

//                 string $drivenAttr - the name of the "driven" node and the attribute 

//                 string $newAttrName - the name of the new attr added to the tensionMeter group

//                                       that allows the user to explicitly change the "driven" attr value

//                 string $groupName = the name of the group that will be created or the name of

//                                     an existing group to be altered

//

//   <directions>   Select two nodes and type "tensionMeterWin()".  You have the option of creating a

//                  new group or adding attributes to an existing group.  Type the name of the new attr

//                  and press ok/add.

//

//                  A parent node by the name of "Meter_Groups" will be created automatically.

//                  The child nodes will contain the tensionMeter attributes.  They are:

//

//                     Additive Meter - on or off. If "on", tensionMeter will use the positive change

//                     in value to calculate the magnitude. The negative 

//                     change in value will produce an attenuation of the magnitude.  If "off", the 

//                     effects will be the same but with the negative change in value as determinant of magnitude. 

//

//                     Add Min Units, Add Units Frame - these attributes define a range in values.

//                     The tension between these two values determine the magnitude in

//                     values from one frame to the next.  Add Min Units is the minimum change in value 

//                     that affects the "driven" attr.  Add Units Frame is the maximum change in

//                     value that affects the "driven" attr.

//

//                     Subtractive Meter - non-keyable.  Reflects the opposite state of Additve Meter attr.

//

//                     Sub Min Units, Sub Units Frame - Serve the same purpose as their Additive

//                     counterparts.

//

//                     Attenuation - 0 to 1 value. Determines the rate at which the magnitude attenuates

//                     when the driver attr is at rest or in the case of additive mode, the change 

//                     in value is negative.

//                     

//                     New Attr, New Attr_scale - these attr give the user explicit control over the 

//                     "driven" attr with the option to scale the value in a positive or negative

//                     direction.
//
//
//
//
//   tMGselect.mel
// 
//   Creates a window for quick access.   

//   This window gives you quick access to your tensionMeter groups.
//   If you have many disparate groups to access, this window will
//   simplify the process of selecting and deleting groups and their 
//   particular expression nodes.
