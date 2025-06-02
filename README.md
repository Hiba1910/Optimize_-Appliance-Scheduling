Optimizing Appliance Scheduling with Simulated Annealing
🧠 Objective
Optimize appliance start times to minimize total user dissatisfaction, which results from deviation between actual and preferred start times.

⚙️ Problem Constraints
Fixed appliance durations

Battery capacity limits

Variable energy generation

User dissatisfaction metrics based on time deviation

🔁 Approach: Simulated Annealing
Initialization:
Start with an initial schedule s = s₀.

Iteration Loop:

Randomly pick one appliance.

Propose a neighboring solution by shifting its start time (±1 hour).

Check validity: battery, generation limits, and constraint compliance.

Evaluate fitness of current and neighbor schedules.

Use Metropolis criterion to decide whether to accept the neighbor:

𝑃
(
𝐸
(
𝑠
)
,
𝐸
(
𝑠
𝑛
𝑒
𝑤
)
,
𝑇
)
P(E(s),E(s 
new
​
 ),T)
Accept better solutions or worse ones with a probability.

Cool down temperature:
temperature *= cooling_rate (geometric cooling)

Repeat for a defined number of iterations.

🔋 Additional Features
Day-by-day simulation

Handling spillover from previous days

Dynamic battery state updates

Fitness evaluations

Daily statistics: deviation percentages and visual summaries

📊 Outputs
Appliance schedules

Visualizations of energy usage vs. energy avaliablity vs battery state with table and plots
