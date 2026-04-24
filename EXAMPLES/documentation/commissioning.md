---
id: "item-xxx"
type: "article"
title: "Commissioning"
status: "published"
version: "1"
language: "en-us"
firstReleaseDate: "2025-11-04"
updateDate: "2025-11-04"
accessLevel: "public"
---

# Commissioning {% tag="commissioning" %}

Commissioning consists of defining, installing, creating, integrating, testing, documenting, and verifying your site and robot system. .The following sections give key points and step-by-step guidance to commission your site and robot system. {% tagref tag="" external_flag=true /%}

Use the commissioning checklist to keep an overview of your commissioning progress—see [Commissioning checklist](commissioning_checklist.htm).

It is the responsibility of the commissioner to draw up the Declaration of Conformity for the entire system, including any partly completed machinery and applying the CE mark to verify that the system is safe and commissioned according to regulatory standards.

**Figure 3.1**Flow diagram of the commissioning process

<image: "overview\_fleet\_txt\_en.svg">

Consider the following points in the process:

  * **Responsibility** : Only assigned persons should be present during commissioning. The commissioner has the main responsibility to ensure the robot is commissioned safely.

  * **Safety** : While commissioning, ensure the safety of all persons present during commissioning.

Do not load the robot, keep a safe distance to the robot, and always keep a visual of the robot in case it does not perform as expected.

  * **Requirements for robot system** : Start by clearly defining the requirements and objectives of the system. Understand the specific tasks, workflows, and challenges that the MiR robots will address.

  * **Iterations** : Commissioning is an iterative process that requires adjustments and frequent testing.

  * **Initial and final risk assessment** : Create a risk assessment of the expected solution to identify any critical safety issues. Any major changes made while commissioning must be evaluated in a new risks assessment. Always make sure that you evaluate the safety of a solution before implementing it. Conduct a final risk assessment to ensure you have implemented all relevant risk mitigation means.

  * **Integration with existing systems** : Evaluate the compatibility of MiR robots with existing systems, such as warehouse management software (WMS), enterprise resource planning (ERP), or other automation systems. Ensure seamless integration to optimize overall operations. Integration-specific commissioning tasks will not be in the guide and depend on the solution and integration design.

  * **Task definition and planning** : Define specific tasks that MiR robots will perform and plan task execution. Consider factors such as task priorities, routes, and any dynamic changes in the environment that the robots need to adapt to.

  * **Mapping and navigation** : Utilize MiR's mapping and navigation capabilities by understanding how maps and zones work, creating an accurate map of the operational area, which considers dynamic obstacles and ensures efficient transportation paths.

  * **User training** : Provide comprehensive training for operators and maintenance personnel. Ensure that they are familiar with the robots, their behavioral patterns, and the basic principles for navigation and dynamic obstacles.

  * **Standalone robot** : You can use a robot in Standalone mode to create the site directly on the robot—see [Interfaces and modes](../../mirfleet/features/standalone_robot.htm). This is useful if you do not want to jump between the robot and MiR Fleet interface while creating the site.

## Desigen review {% tag="review_design" %}

Before implementing any robot setup, ensure that the design plans for the project have been reviewed and verified.

You can use the project design template from the MiR Support Portal to help document your project and consider all relevant points when implementing a MiR system: <https://supportportal.mobile-industrial-robots.com/documentation/commissioning-guides/project-design-review-template/>.

Store the documentation of the design review for at least 10 years and make it available upon request.

While planning your project, conduct an initial risk assessment to evaluate risks and determine suitable mitigation means.

## Checklist

Use the commissioning checklist as a guidance for the commissioning process. The list does not cover all necessary considerations to declare your installation safe and reliable. Additional items can be added based on the specific application or end user needs.

{% table %}

 * Plan solution
 * Comments

---

 * Define the requirements and expectations for the MiR project. See Review design. Fill out the MiR Project Design template to describe your MiR project. The MiR Application team can help review the robot system design to determine its feasibility. Conduct an initial risk assessment of the expected solution. Determine how you will meet the requirements you have set. Evaluate if the requirements are realistic.

 *

---

 * Adjust your site to meet the operating requirements for MiR robots. See Evaluate environment. Measure the smallest areas and verify they meet the robots' space requirements. Test the robots on all driving surfaces and inclines, including gaps and steps, and identify if any areas require special driving behavior. Modify areas with direct lighting, reflective surfaces, or transparent obstacles that may interfere with the robots' sensor system. Evaluate if the site meets all environmental specifications for MiR robots. Check your site for missing, broken, or faulty equipment. Determine where you can install charging stations, load transfer stations, and a service area if relevant.

 *

---

 * Purchase or design a top module for the robot tasks. See Design top modules. Determine which electrical interfaces on the robot the top module will need. Choose a top module design that is compatible with your MiR robots. Evaluate if the combined top module and robot application meets relevant standards.

 *

---

 * Purchase or design load transfer stations, other relevant stations, shelves, or carts for MiR robots. See Design load transfer stations, carts and shelves. Ensure the station, cart, shelf, or rack meets requirements. Determine suitable markers or ID tags for each station or payload. Assess if there is enough space around stations, pick up, and drop off locations for the MiR robot to maneuver.

 *

---

 * Determine the software version you want to use for the MiR system. See Select software. Determine which software version best suits your site.

 *

{% /table %}

{% table %}

 * Set up MiR Fleet
 * Comments

---

 * Configure your network and server to meet the MiR system requirements. See Meet system requirements. Make sure your server and network structure meet the requirements for MiR systems. Ensure robots have a fixed IP address using a method that is approved by your IT department.

 *

---

 * Install MiR Fleet on a prepared server. See Install MiR Fleet. Remove previous MiR Fleet software versions. Install Microsoft .NET Server Hosting and Microsoft SQL server. Create a user to run MiR Fleet Windows Service. Install MiR Fleet on the selected host server.

 *

---

 * Configure MiR Fleet according to site cybersecurity policies and preferences. See Configure MiR Fleet. Configure firewalls, TLS, and SSO. Connect an SQL database.

 *

---

 * Sign in the first time. See Sign in. Sign in to the MiR Fleet interface. Create an admin user.

 *

{% /table %}

{% table %}

 * Set up users
 * Comments

---

 * Create roles and users with the necessary permissions to complete user tasks. See Create users and roles. List all the users for the MiR system and identify which permissions they need to complete their tasks. Identify permissions that enable users to make critical changes. Create roles for each permission group or user type. Create a user in MiR Fleet for each user and assign the user to relevant roles. Test that all users have access to the features and tools they need. Test that users do not have access to anything they are not trained to handle. Document the overview of users, permissions, and tasks.

 *

---

 * Make dashboards to collect relevant functions on a single page in the interface. See Create dashboards. Determine what functions your users need to complete their tasks. Create dashboards that make these tasks easier to complete. Test that your dashboards work as expected. Document which tasks or user each dashboard is intended for.

 *

{% /table %}

{% table %}

 * Manage robots
 * Comments

---

 * For each robot, check the robot's condition and set up the robots to prevent unauthorized access. See Prepare robots. Go through the received product inspection checklist. Upgrade the robot software. Protect against booting up from USB. Set a password for the robot BIOS. Disable all unused features. Disable or password protect robot access points. Update robot access points.

 *

---

 * Connect robots to MiR Fleet. See Add robots. Connect robots to the same Wi-Fi network as MiR Fleet. Set up mutual trust between MiR Fleet and the robots. Add one robot to MiR Fleet to use to setup and test the site with a single robot. When the site is complete and tested, add all other robots to MiR Fleet.

 *

---

 * Adjust the Wi-Fi network so robots have a stable connection across the whole site. See Evaluate Wi-Fi. Review the network requirements for MiR systems. Apply necessary adjustments to your site network. Send two robots across the site to gather Wi-Fi signal data. Evaluate the Wi-Fi performance and coverage. Document the Wi-Fi heatmaps made between any changes to the site network.

 *

---

 * Create groups to define which missions, charging stations, and Staging positions each robot can be assigned to. See Create groups. Determine which charging stations, Staging positions, and missions you want each robot to be compatible with. Create groups that enable each robot to access the necessary resources and missions. Add robots and resources to groups. Document the overview of groups, robots, and resources. Document how to determine which group new elements should be added to.

 *

---

 * Verify that robots are correctly managed by MiR Fleet. See Test MiR Fleet. Verify that data synchronizes correctly across all robots. Test that robots are assigned to missions as expected. Test that robots are assigned to charging stations and Staging positions as expected. Test that robots still run correctly after turning them off and on again.

 *

{% /table %}

{% table %}

 * Set up navigation
 * Comments

---

 * Record or upload accurate floor plans. See Create floor plans. Determine your floor plan strategy. If you are recording any floor plans, prepare the operating area. Optimize the floor plan quality. Remove invalid floor plans from MiR Fleet.

 *

---

 * Combine floor plans to create maps. See Create maps. Determine the number of maps you need to cover the operating area. Determine the naming scheme for your maps. Align floor plans and merge them together to create a straight map. Add or remove obstacles to make the maps accurate. Document which areas each map covers.

 *

---

 * Ensure robots can localize themselves across the whole operating area. See Evaluate localization. Localize all robots on the active map. Drive one robot across the whole map. Evaluate the localization score. Apply map changes if necessary. Document the final localization score and evaluate the localization regularly to ensure the map continues to be accurate.

 *

---

 * Create transitions between maps. See Create transitions. Create transition positions where maps overlap. Create transition missions for each map transition. Define transitions. Test that a robot can travel to and from each map using the appropriate transition. Document the transitions, including the relevant map locations, positions, and missions.

 *

{% /table %}

{% table %}

 * Program robot tasks
 * Comments

---

 * Define the robot tasks and break them down into mission building blocks and categories. See Define tasks. List all robot tasks. Define the actions the robots must perform to complete the tasks. Identify actions that are repeated across tasks. Plan how you want to organize missions into mission groups. Agree on a naming scheme.

 *

---

 * Create markers and positions at all points of interest for the robot tasks. See Create positions and markers. Determine which type of position or marker is best suited for each point. Agree on a naming scheme. Add positions and markers. Test how the robot docks to each marker and apply corrections.

 *

---

 * Create mission groups and missions for the robot tasks. See Create missions and mission groups. Create the mission groups you planned. Create reusable missions for all actions that are repeated across robot tasks. Create missions for the robot tasks. Test the missions and apply corrections. Document the mission setup.

 *

---

 * Make missions more robust. See Make missions robust. Test missions where you expose the robot to unexpected events you want it to handle autonomously. Use Try/Catch actions to define alternative actions in missions when exceptions or unexpected events occur. Iterate between testing and modifying missions. Update the mission documentation if necessary.

 *

---

 * Set up system for scheduling missions. See Schedule missions. Determine triggers for each mission. Create or modify any external system to schedule missions automatically. Create or modify dashboards to help users schedule missions manually. Document the chosen triggers for each mission and responsibilities for ensuring each mission runs.

 *

{% /table %}

{% table %}

 * Configure path planning
 * Comments

---

 * Create footprints that make robots plan efficient paths that avoid collisions. See Create footprints. Determine the dimensions of all the possible top modules and loads on the MiR robots. Agree on a naming scheme that makes it clear which footprint to use. Create footprints. Document the size and purpose of each footprint.

 *

---

 * Add zones to maps to make MiR Fleet prevent robots from blocking each other and prevent robots from driving into unintended areas. See Manage traffic. Mark points of interest, robot routes, existing traffic conditions, and other relevant factors on a map of the operating area. Use Preferred, Unpreferred, and Directional zones to coordinate the robot routes. Use Forbidden zones to designate areas that you want the robot to plan around. At all crossings, docking stations, and narrow corridors, use Limit-robots zones to prevent robots blocking each other. Document all of the zones and their purposes.

 *

---

 * Adjust the robot settings to change how the robot drives and plans paths. See Configure settings. Define how much robots can deviate in their path planning. Determine if you need to adjust the camera filtering settings. Apply settings changes to all other relevant robots.

 *

{% /table %}

{% table %}

 * Assess safety
 * Comments

---

 * Conduct a risk assessment. See Conduct risk assessment. Use the MiR Risk Assessment Guide for MiR-specific use cases. You can find this document on MiR Support Portal.

 *

---

 * Implement risk mitigation means. See Mitigate risks. Mark high-risk areas as operating hazard zones. Mark all docking and charging areas as operating hazard zones. Implement lights and sounds in the robot maps and missions to increase personnel awareness. Design docking areas to include escape routes for personnel.

 *

---

 * Ensure the robots' braking distance is safe with all loads. See Test braking distance. Conduct a brake test with the lightest, heaviest, and largest loads, and any loads with unusual properties. Adjust the robot, the environment, or the robot payload until the stopping distance criteria in the brake test are met.

 *

{% /table %}

{% table %}

 * Ensure security and stability
 * Comments

---

 * Assess the cybersecurity of your MiR system. See Evaluate cybersecurity. Conduct a cybersecurity risk assessment. Protect the robots from unauthorized access. Manage users Implement an auditing system

 *

---

 * Document emergency plans for all potential emergency situations. See Define emergency plans. Identify possible emergency situations. Implement preventative actions to reduce the likelihood and severity of the emergency. Document what must be done and who is responsible for each task if the event should occur.

 *

---

 * Monitor site events and analyze data for performance improvements and unintended or suspicious behavior. See Monitor system. Determine relevant monitoring tools and information. Define behavior to be acted on. Set up filters on Event viewer to detect relevant messages in MiR Fleet. Set up an application to monitor important messages from MiR Fleet audit log. Define responsibilities for incoming alerts. Consider setting up webhook subscriptions to events of interest. Consider purchasing a MiR Insights license and determine what data you can use.

 *

{% /table %}

{% table %}

 * Prepare handover
 * Comments

---

 * Ensure your MiR system conforms to relevant standards to maintain a safe solution. See Assess conformity. Assess the system conformity regularly against the latest relevant standards. Collect a technical file with all relevant system documentation and information of use for the complete system. Establish a maintenance schedule. Assess any custom top module or modification made to approved top modules.

 *

---

 * Train users so they can correctly and safely execute tasks they are responsible for. See Train users. Determine the responsibilities of your users and categorize them into user types. Train users in their relevant tasks and knowledge of the MiR system. Keep training records and schedule new training sessions if new equipment or processes are introduced.

 *

{% /table %}
