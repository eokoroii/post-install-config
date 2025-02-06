<h1>osTicket Lab 2: Roles, Departments, Teams & Help Topics</h1>

<h2>Project Summary</h2>
<p>
  With osTicket installed, the next step is configuring <strong>Roles</strong>, 
  <strong>Departments</strong>, <strong>Teams</strong>, <strong>SLAs</strong>, 
  and <strong>Help Topics</strong>. These settings define how agents interact 
  with tickets, which departments handle certain issues, and how tickets are categorized 
  and prioritized.
</p>

<ul>
  <li><strong>Focus Areas:</strong>
    <ul>
      <li>Agent Roles &amp; Permissions</li>
      <li>Department creation (top-level vs. nested)</li>
      <li>Team creation (cross-department collaboration)</li>
      <li>SLA Plans (Sev-A, Sev-B, Sev-C)</li>
      <li>Help Topics (e.g., Business Critical Outage, Equipment Request)</li>
    </ul>
  </li>
  <li><strong>Outcome:</strong> 
    A well-structured osTicket instance that routes tickets to the right people 
    and enforces relevant service-level agreements.
  </li>
</ul>

<hr />

<h2>Steps & Screenshots</h2>
<ol>
  <li>
    <strong>Admin vs. Agent Panel</strong><br />
    After logging in with admin credentials, I briefly compared the <em>Admin Panel</em> 
    (system-wide settings) vs. the <em>Agent Panel</em> (daily ticket operations).
    <br /><br />
    <p align="center">
      <img src="https://i.imgur.com/2hgo65U.png" alt="Admin Panel overview" width="600" />
      <br />
      <em>Figure 3.1 – Admin Panel has system-level controls.</em>
    </p>
  </li>
  <br />

  <li>
    <strong>Creating a New Role: Supreme Admin</strong><br />
    In <em>Agents &gt; Roles</em>, I clicked <em>+Add New Role</em> and named it <code>Supreme Admin</code>, 
    granting full permissions (Tickets, Tasks, Knowledgebase) as a demonstration of maximum privileges.
    <br /><br />
    <p align="center">
      <img src="https://i.imgur.com/EnQefgH.png" alt="Creating new role" width="600" />
       <img src="https://i.imgur.com/8OYspZn.png" alt="Creating new role" width="600" />
      <br />
      <em>Figure 3.2 – Defining permissions for Supreme Admin role.</em>
    </p>
  </li>
  <br />

  <li>
    <strong>Reviewing Other Roles</strong><br />
    osTicket comes with default roles like <em>Limited Access</em> or <em>View Only</em>. 
    I quickly reviewed their permissions to see how they differ from the new <code>Supreme Admin</code>.
    <br /><br />
    <p align="center">
      <img src="https://i.imgur.com/wNljok1.png" alt="Default roles in osTicket" width="600" />
      <br />
      <em>Figure 3.3 – Built-in roles overview.</em>
    </p>
  </li>
  <br />

  <li>
    <strong>Departments Setup</strong><br />
    Departments group agents by function (e.g., Support, Billing, SysAdmins). 
    Under <em>Agents &gt; Departments</em>, I clicked <em>+Add New Department</em> 
    and named one <code>Sysadmin</code>, setting its parent to <em>Top-Level</em>.
    <br /><br />
    <p align="center">
      <img src="https://i.imgur.com/2nBvwRS.png" alt="Adding Sysadmin dept" width="600" />
      <br />
      <em>Figure 3.4 – Creating Sysadmin department.</em>
    </p>
  </li>
  <br />

  <li>
    <strong>Teams Setup</strong><br />
    Teams can span multiple departments. Under <em>Agents &gt; Teams</em>, 
    I added a new team named <code>Online Banking</code> so that agents from different departments 
    can collaborate on banking-related tickets.
    <br /><br />
    <p align="center">
      <img src="https://i.imgur.com/617RwtC.png" alt="Team creation" width="600" />
      <br />
      <em>Figure 3.5 – Creating the Online Banking team.</em>
    </p>
  </li>
  <br />

  <li>
    <strong>Editing User Registration Settings</strong><br />
    In <em>Admin Panel &gt; Settings &gt; Users</em>, I unchecked <em>Registration Required</em> 
    so that unregistered users can still create tickets. This helps in scenarios where quick ticket creation 
    is vital.
    <br /><br />
    <p align="center">
      <img src="https://i.imgur.com/PXd8TeI.png" alt="User settings" width="600" />
      <br />
      <em>Figure 3.6 – Adjusting user registration preferences.</em>
    </p>
  </li>
  <br />

  <li>
    <strong>Creating Agents</strong><br />
    Under <em>Agents &gt; +Add New Agent</em>, I created:
    <ul>
      <li><strong>Jane Doe</strong> – Department: Sysadmin, Role: Supreme Admin, Team: Online Banking</li>
      <li><strong>John</strong> – Department: Support, Role: View Only</li>
    </ul>
    <p align="center">
      <img src="https://i.imgur.com/G6IObGI.png" alt="Add new agents" width="600" />
      <img src="https://i.imgur.com/dax1fSw.png" alt="Add new agents" width="600" />
      <img src="https://i.imgur.com/Xl1pijG.png" alt="Add new agents" width="600" />
      <br />
      <em>Figure 3.7 – Assigning roles and departments to agents.</em>
    </p>
  </li>
  <br />

  <li>
    <strong>Creating End Users from the Agent Panel</strong><br />
    From the <em>Agent Panel &gt; Users &gt; +Add User</em>, I added at least two end users 
    (Ken & Karen). End users can open tickets without needing agent-level permissions.
    <br /><br />
    <p align="center">
      <img src="https://i.imgur.com/bJX4peP.png" alt="Add user in agent panel" width="600" />
      <img src="https://i.imgur.com/1KxQFX0.png" alt="Add user in agent panel" width="600" />
      <br />
      <em>Figure 3.8 – Creating an end user for ticket submissions.</em>
    </p>
  </li>
  <br />

  <li>
    <strong>Configuring SLA Plans</strong><br />
    Under <em>Manage &gt; SLA</em>, I created:
    <ul>
      <li><code>Sev-A</code> – 1-hour grace, 24/7 schedule</li>
      <li><code>Sev-B</code> – 4-hour grace, 24/7</li>
      <li><code>Sev-C</code> – 8-hour grace, M-F 8am-5pm + holidays</li>
    </ul>
    <p align="center">
      <img src="https://i.imgur.com/AOgKZab.png" alt="SLA plan setup" width="600" />
      <img src="https://i.imgur.com/4zGqVc4.png" alt="SLA plan setup" width="600" />
      <br />
      <em>Figure 3.9 – Adding multiple SLA Plans for different urgency levels.</em>
    </p>
  </li>
  <br />

  <li>
    <strong>Defining Help Topics</strong><br />
    Finally, in <em>Manage &gt; Help Topics</em>, I added:
    <ul>
      <li><code>Business Critical Outage</code> (parent: Report a Problem)</li>
      <li><code>Personal Computer Issues</code> (parent: Report a Problem)</li>
      <li><code>Equipment Request</code> (parent: General Inquiry)</li>
      <li><code>Password Reset</code> (parent: Report a Problem)</li>
      <li><code>Other</code> (parent: General Inquiry)</li>
    </ul>
    <p align="center">
      <img src="https://i.imgur.com/u9B3gSl.png" alt="Creating help topics" width="600" />
      <img src="https://i.imgur.com/iV5ZbKz.png" alt="Creating help topics" width="600" />
      <br />
      <em>Figure 3.10 – Help topics let end users categorize their issues more easily.</em>
    </p>
  </li>
</ol>

<hr />

<h2>Conclusion</h2>
<p>
  By setting up roles, departments, teams, SLAs, and help topics, I prepared osTicket 
  for a real-world help desk environment. Agents now have the correct permissions, 
  tickets can be escalated according to SLA urgency, and end users have relevant categories 
  to classify their requests. Next up: seeing these configurations in action with 
  real ticket creation and resolution!
</p>
