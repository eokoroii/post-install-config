<p align="center">
  <!-- Replace this with a banner or keep the osTicket logo -->
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket Logo" width="200"/>
</p>

<h1>osTicket Post-Install Configuration Lab</h1>

<h2>Project Summary</h2>
<p>
   In this lab, I walked through adjusting global settings, 
  setting up email piping, creating departments and teams, and ensuring the security 
  configuration was suitable for a production-like environment.
</p>
<p>
  My goal was to demonstrate not only how to get osTicket running, 
  but also how to tailor it to fit a typical organization’s help desk workflow.
</p>

<ul>
  <li>
    <strong>Technologies &amp; Services Involved:</strong>
    <ul>
      <li>osTicket Admin Panel (Staff Control Panel)</li>
      <li>MySQL Database</li>
      <li>SMTP / IMAP / POP Email Services</li>
      <li>PHP (ini / extension configs if needed)</li>
    </ul>
  </li>
  <li>
    <strong>Key Objectives:</strong>
    <ul>
      <li>Adjust and personalize core system settings</li>
      <li>Configure email templates, notifications, and ticket intake</li>
      <li>Set up departments, teams, and user roles for effective ticket routing</li>
      <li>Establish advanced features like SLAs (Service Level Agreements)</li>
    </ul>
  </li>
</ul>

<hr />

<h2>Steps &amp; Screenshots</h2>
<ol>
  <li>
    <strong>Accessing the Admin Panel</strong><br />
    To kick things off, I logged into the osTicket <em>Staff Control Panel (scp)</em> at 
    <code>http://&lt;my_server&gt;/osticket/scp</code>. 
    From the dashboard, I immediately headed to <em>Admin &gt; Settings</em> to review and fine-tune 
    the global preferences, such as help desk name, default email address, and system URL. 
    Making these changes gave the help desk a more personalized identity.
    <br /><br />
    <img src="(SCREENSHOT #1)" alt="Admin Panel Overview" width="600" />
  </li>
  <br />

  <li>
    <strong>Customizing System Settings &amp; Brand Identity</strong><br />
    Under <em>Admin &gt; Settings &gt; Company</em>, I replaced all default placeholders with my 
    own organization info:
    <ul>
      <li><em>Helpdesk Name:</em> e.g., “IT Support Desk”</li>
      <li><em>Default System Email:</em> e.g., <em>support@myorg.com</em></li>
      <li><em>Organization Logo/Name:</em> for a polished user experience</li>
    </ul>
    This ensured that tickets and emails displayed consistent branding.
    <br /><br />
    <img src="(SCREENSHOT #2)" alt="Company Settings" width="600" />
  </li>
  <br />

  <li>
    <strong>Configuring Email Piping &amp; Notification Settings</strong><br />
    Next, I focused on email-related configuration in <em>Admin &gt; Emails &gt; Emails</em>. 
    Here’s what I did:
    <ul>
      <li>Added a support inbox <em>(support@myorg.com)</em> to handle incoming tickets</li>
      <li>Enabled <em>SMTP</em> to ensure outgoing notifications were sent reliably</li>
      <li>Tested these settings by sending a few test emails to confirm tickets were created</li>
    </ul>
    Once I saw those test messages auto-generate tickets, I knew the system was set up correctly.
    <br /><br />
    <img src="(SCREENSHOT #3)" alt="Email Configuration" width="600" />
  </li>
  <br />

  <li>
    <strong>Defining Departments, Teams, &amp; Agents</strong><br />
    I wanted to reflect a real help desk structure, so under <em>Admin &gt; Agents</em> and 
    <em>Admin &gt; Departments</em>, I created:
    <ul>
      <li>
        <em>Departments:</em> 
        <ul>
          <li>IT Support</li>
          <li>Human Resources</li>
          <li>Customer Service</li>
        </ul>
      </li>
      <li>
        <em>Agents:</em> assigned each staff member to the relevant department, ensuring tickets 
        route correctly.
      </li>
      <li>
        <em>Teams:</em> optional groups for cross-department collaboration, if needed.
      </li>
    </ul>
    This setup ensures that tickets land where they need to go without manual intervention.
    <br /><br />
    <img src="(SCREENSHOT #4)" alt="Departments & Agents Setup" width="600" />
  </li>
  <br />

  <li>
    <strong>Establishing SLAs &amp; Help Topics</strong><br />
    Under <em>Admin &gt; Manage &gt; SLA Plans</em>, I set up different response-time goals—for example, 
    “Urgent” tickets had a 1-hour response target while “Normal” had 4 hours. 
    I also defined some <em>Help Topics</em> (<em>“Password Reset,” “Hardware Issue,” “Benefits Inquiry”</em>), 
    so incoming tickets would be categorized automatically. 
    This step ensures better organization and accountability.
    <br /><br />
    <img src="(SCREENSHOT #5)" alt="SLA and Help Topics" width="600" />
  </li>
  <br />

  <li>
    <strong>Email Templates &amp; Alerts</strong><br />
    Next, I dove into <em>Admin &gt; Emails &gt; Templates</em> to tweak the default email messages 
    sent to users and agents. For a more professional touch, I modified the wording in the “New Ticket Alert” 
    and “Ticket Response” templates. I also checked <em>Alerts &amp; Notices</em> to confirm which 
    email notifications were triggered for various ticket events.
    <br /><br />
    <img src="(SCREENSHOT #6)" alt="Email Templates" width="600" />
  </li>
  <br />

  <li>
    <strong>Reviewing Security &amp; Access Controls</strong><br />
    Under <em>Admin &gt; Security Settings</em>, I confirmed that password policies (minimum length, 
    complexity) and session timeouts were in line with best practices. I also verified that the 
    correct permissions were set for staff roles, preventing unauthorized access to sensitive 
    admin options or plugin management.
    <br /><br />
    <img src="(SCREENSHOT #7)" alt="Security Settings" width="600" />
  </li>
  <br />

  <li>
    <strong>Final Testing &amp; Verification</strong><br />
    Lastly, I created a test ticket via the user portal to see the entire process in action:
    <ul>
      <li>A user-facing form captured the issue details</li>
      <li>An auto-generated email notified me (as the assigned agent)</li>
      <li>My agent response triggered another email back to the user</li>
    </ul>
    Everything flowed smoothly, confirming that my configurations were correct.
    <br /><br />
    <img src="(SCREENSHOT #8)" alt="Test Ticket and Notifications" width="600" />
  </li>
</ol>

<hr />

<h2>Conclusion</h2>
<p>
  By walking through these post-install configuration steps, I ensured that 
  my osTicket deployment wasn’t just set up, but actively customized for real-world 
  service desk operations. From branding and email flow to user roles and security protocols, 
  every detail I configured helps streamline support workflows and maintain a secure, 
  efficient help desk system. 
</p>
<p>
  If you have questions or suggestions about this lab process, feel free to reach out or open an issue!
</p>
