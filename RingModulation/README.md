# RingModulation

ring modulation : 2 in (to_rm_x1) / 2 out (from_rm_x2)

with x1 = 2*@-1 and x2 = 2*@

argument : @ : number of the instance

# osc address :  /rm@
                    /fq
                        /L [0. - 15 000.]
                        /R [0. - 15 000.]
                    /outgain [-70. - 6.]
                    /preset

all messages can have 3 formats :
    one number : arrival value, get there in 10ms
    two numbers : arrival value, time
    three number : beginning value, arrival value, time
    more numbers : create a break point function with the given values as equidistant points, the last one being the time it takes for the line object to go through the BPF
DO NOT PUT COMMAS IN YOUR MESSAGES ; otherwise it sends multiple messages

example of a correct osc message :
osc /rm1/fq/L 50. 100. 5000
it changes the frequency of the modulation of the left channel from 50 Hz to 100 Hz in 5 seconds