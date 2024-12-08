% Constants for state representation
OFF = 1;
WASHING = 2;
% Initialize the washing machine state
machineState = OFF;
% Number of iterations to run in each state
offIterations = 3; % Example: 3 iterations in the OFF state
washingIterations = 5; % Example: 5 iterations in the WASHING state
% Set up progress bar
totalIterations = offIterations + washingIterations;
progressBarWidth = 30;
% Main loop
for iteration = 1:totalIterations
fprintf('\n');
% Display washing machine status with dynamic color and ASCII art
if machineState == OFF
fprintf('\x1b[33m ___\n');
fprintf(' | ___ |\n');
fprintf(' | | | |\n');
fprintf(' | | OFF | |\n');
fprintf(' | |___| |\n');
fprintf(' |___|\x1b[0m\n');
if iteration >= offIterations
machineState = WASHING;
end
elseif machineState == WASHING
fprintf('\x1b[36m ___\n');
fprintf(' | ___ |\n');
fprintf(' | | | |\n');
fprintf(' | | WASHING | |\n');
fprintf(' | |___| |\n');
fprintf(' |___|\x1b[0m\n');
if iteration >= (offIterations + washingIterations)
machineState = OFF;
end
end
% Update progress bar with dynamic color and a washing-related
symbol
progress = floor(iteration / totalIterations * progressBarWidth);
progressBar = sprintf('[\x1b[32m%s\x1b[0m%s]', repmat('~', 1,
progress), repmat('.', 1, progressBarWidth - progress));
fprintf('\nProgress: %s\n', progressBar);
% Display detailed state information with dynamic color
if machineState == OFF
fprintf('\n\x1b[33mWashing machine is OFF\x1b[0m\n');
% Additional OFF state actions can be added here
elseif machineState == WASHING
fprintf('\n\x1b[36mWashing machine is WASHING\x1b[0m\n');
% Additional WASHING state actions can be added here
end
% Add a pause to simulate real-time progression
pause(0.5);
% Clear the command window for a cleaner display (comment out if
not needed)
clc;
end
fprintf('\nWashing machine simulation completed.\n');
