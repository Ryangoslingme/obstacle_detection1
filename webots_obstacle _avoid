from controller import Robot

# Initialize the robot
robot = Robot()

# Get basic simulation timestep
TIMESTEP = int(robot.getBasicTimeStep())
MAX_SPEED = 6.28  # Maximum velocity for e-puck wheels in rad/s

# Initialize Motors
left_motor = robot.getDevice('left wheel motor')
right_motor = robot.getDevice('right wheel motor')

# Set motor mode to velocity mode (position = infinity)
left_motor.setPosition(float('inf'))
right_motor.setPosition(float('inf'))

# Initialize motor velocities to zero
left_motor.setVelocity(0.0)
right_motor.setVelocity(0.0)

# Initialize Distance Sensors (DistanceSensors ps0 through ps7)
list_ps = []
for ind in [0, 1, 2, 5, 6, 7]:
    sensor_name = 'ps' + str(ind)
    ps_sensor = robot.getDevice(sensor_name)
    ps_sensor.enable(TIMESTEP)
    list_ps.append(ps_sensor)

# Main Loop
while robot.step(TIMESTEP) != -1:
    # Default forward speed
    left_speed = MAX_SPEED
    right_speed = MAX_SPEED

    # Read proximity sensors
    for ps in list_ps:
        ps_val = ps.getValue()
        
        # If an obstacle is detected nearby (threshold > 100)
        if ps_val > 75:
            # Turn the robot by altering wheel direction
            left_speed = -MAX_SPEED
            right_speed = MAX_SPEED

    # Send motor commands
    left_motor.setVelocity(left_speed)
    right_motor.setVelocity(right_speed)
