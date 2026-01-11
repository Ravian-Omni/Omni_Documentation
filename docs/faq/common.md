# Common Questions

---

## General

???+ question "What is Ravian AI?"

    Ravian AI is a device-native autonomous AI agent powered by Large Action Models (LAMs). It understands goals, plans multi-step workflows, and executes them across apps, files, and web services on your local machine.

??? question "How is Ravian different from other AI tools?"

    Unlike chat-based AIs that generate text responses, Ravian executes actions — opening apps, filling forms, creating files, sending emails, and completing workflows end-to-end. It thinks in steps, not single answers.

??? question "Is Ravian safe to use?"

    Yes. Ravian includes:

    - Human approvals for sensitive actions such as emails, forms, and file changes  
    - Built-in validation that checks its own work  
    - Device-native execution to keep data local  
    - Configurable guardrails for enterprise environments  

??? question "Does Ravian run on my device or in the cloud?"

    Ravian runs entirely on your device. Your data, files, and workflows never leave your machine. It controls your local apps and browser through standard desktop automation.

---

## Installation & Setup

??? question "What operating systems are supported?"

    Ravian works on Windows and macOS. Download the appropriate installer from https://www.ravian.ai.

??? question "Do I need special hardware?"

    No. Ravian uses your existing hardware. For optimal performance with long workflows or multimodal tasks, 16 GB RAM and a modern processor are recommended.

??? question "Can I use Ravian behind a corporate firewall?"

    Yes. You may need to allow Ravian through your firewall, configure proxy settings for web access, and approve app permissions for controlled applications. Contact your IT team if you encounter connectivity issues.

??? question "How do I update Ravian?"

    Ravian checks for updates automatically. Click Help → Check for Updates in the menu, or it will prompt you when a new version is available.

---

## Usage & Workflows

??? question "What should I ask Ravian to do?"

    Think in terms of complete outcomes.

    ```text
    ❌ "Search for X"
    ✅ "Research X market and create a 10-slide summary deck"

    ❌ "Analyze this data"
    ✅ "Load sales.csv, find top trends by region, and create an executive report"
    ```

??? question "How specific do my instructions need to be?"

    Start broad, then refine. Ravian plans first and shows you what it intends to do. You can edit the plan or add constraints before approving execution.

??? question "Can Ravian access my private files or accounts?"

    Yes, but only with your explicit approval. Sensitive actions trigger an approval dialog where you review exactly what Ravian intends to access or modify.

??? question "What happens if a workflow fails midway?"

    Ravian’s validation system:

    - Retries failed steps  
    - Switches data sources when primary ones fail  
    - Surfaces clear errors with suggested fixes  
    - Saves partial progress so you can resume  

??? question "Can multiple people use Ravian on the same machine?"

    Yes. Each user gets their own workspace, approval settings, and task history. Admin permissions may be needed for initial installation.

---

## Capabilities

??? question "Can Ravian really build complete presentations from scratch?"

    Yes. Ravian can research the content, create slide structure and copy, generate charts and visuals, and export to PowerPoint or Google Slides formats.

??? question "Does Ravian write code?"

    Yes. Ravian writes, tests, and debugs Python, JavaScript, and HTML/CSS for data analysis, automation, and application workflows.

??? question "Can Ravian handle video or images?"

    Yes. Ravian supports:

    - Video transcription and summarization  
    - Image analysis and generation  
    - Audio-to-text conversion  
    - Multimodal workflows combining all formats  

??? question "How does Ravian know which job listings match my criteria?"

    You define filters once. Ravian applies them consistently across boards and tracks applications in a structured log.

---

## Privacy & Security

??? question "Where does my data go?"

    Nowhere. Ravian processes everything locally. Web requests go through your browser. Files remain on your device.

??? question "Can Ravian accidentally send wrong emails?"

    No. Email actions always require approval. You review recipients, subject, and content before anything is sent.

??? question "What permissions does Ravian need?"

    Ravian requests standard desktop automation permissions including application control, folder access, and screen capture. Microphone and camera access are optional and used only for multimodal workflows.

??? question "Is there an enterprise version?"

    Yes. Enterprise deployments include volume licensing, SSO integration, centralized policy management, and audit logging. Contact reachus@ravian.ai for details.

---

## Troubleshooting

??? question "Ravian won't launch"

    Ensure all permissions were granted during installation. Try running as administrator on Windows, restart the system, or reinstall from ravian.ai.

??? question "Tasks keep failing on web pages"

    Clear browser cache and cookies, disable ad blockers temporarily, ensure your default browser is set correctly, and check corporate firewall or proxy settings.

??? question "Approvals aren't working"

    Verify in Settings → Safety that approval rules are enabled for the expected action types. Test with a simple email task.

??? question "How do I reset my workspace?"

    Settings → Advanced → Reset Workspace clears task history, cached files, and settings while keeping the core application intact.

---

## Billing & Support

??? question "Is there a free version?"

    Yes. Ravian offers a free tier for personal use with generous limits. Paid plans unlock advanced features and priority support.

??? question "How do I get help?"

    Support is available via documentation at docs.ravian.ai, email at reachus@ravian.ai, community channels inside the app, and priority support for Pro and Enterprise plans.

    If you still need help, email reachus@ravian.ai with details about your workflow and issue.
