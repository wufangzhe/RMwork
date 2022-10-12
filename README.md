# RMwork
RMwork
第二次作业
#include<iostream>
using namespace std;
int main()
{
    int i,x;
    cin>>x;
    for(i=1;i<=x;i++)          //i的循环结构
    {
        cout<<"Hello,Robomaster!"<<endl;
    }
    return 0;
}
                                        
                                        
                                        
                                        
第三次作业
#include "ros/ros.h"
#include "geometry_msgs/Twist.h"
int main(int argc,char *argv[])
{
    //pub msgs to control the turtle                                            
    //topic:/turtle1/cmd_vel                                                    
    //type:geometry_msgs/Twist                                                  
    //step:include the head file                                                
    //initialize  ros node                                                      
    //create handle of ros                                                      
    //create pub                                                                
    ros::init(argc,argv,"mycotrol"); //initialize node                          
    ros::NodeHandle nh;
    ros::Publisher pub = nh.advertise<geometry_msgs::Twist>("/turtle1/cmd_vel",\
10);
    ros::Rate rate(10);
    geometry_msgs::Twist twist;
    twist.linear.x = 1.0;
    twist.linear.y = 0.0;
    twist.linear.z = 0.0;
    twist.angular.x = 0.0;
-UU-:----F1  pub_control_msg
