**Init/Shutdown Script**

{{< truetable >}}
| Name | Description |
|------|-------------|
| **Description** | Comments about this script. |
| **Type** | Select **Command** for an executable command or **Script** for an executable script. |
| **Command** | Enter the command with any options. When **Script** is selected, click the <i class="material-icons" aria-hidden="true" title="folder">folder</i> to define the path to the script file. |
| **When** | **Pre Init** is early in the boot process, after mounting filesystems and starting networking. **Post Init** is at the end of the boot process, before TrueNAS services start. **Shutdown** is during the system power off process. |
| **Enabled** | Enable this task. Clear to disable the task without deleting it. |
| **Timeout** | Automatically stop the script or command after the specified seconds. |
{{< /truetable >}}
