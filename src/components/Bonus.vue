<template>
    <div class="centered-marge">
      <div id="article">
        <h4 class="verdanaH">Linux as a desktop OS</h4>                  
        <p> Linux works well on server. However on desktop, there are more things to consider: multimedia codecs, Wi-Fi drivers, GPU drivers (possible screen tearing/stuttering/flickering), CPU microcode, printers drivers, ... Problems may happen. Never expect popular distros to make things work out-of-the-box as they pretend to do. Better study the configuration files and CLI utilities by reading the <a href="https://wiki.archlinux.org/title/Main_page">Arch wiki</a> or the Gentoo wiki. A good Linux user doesn't need GUI tools besides the installer.<br> Opinions about bloat are divided. Security experts think that complex software is prone to vulnerabilities. Some pieces of software contain tremendous amounts of totally unnecessary attack surface and follows poor security practices. In addition, new features can increase the attack surface and introduce a large amount of new bugs. <a href="https://www.gnu.org/distros/free-distros.en.html">FSF-approved</a> Trisquel GNU/Linux gives a good idea about what to avoid. Trisquel doesn't have a Gnome edition, so I don't use Gnome. My favorite distro is Void Linux. This distro is praised for its speed, small attack surface, and flexibility.</p>
        
            
            <div class="myrow">
              <div class="column padding">
                <p class="fun-font ">click here to enter the void</p>
              </div>
            
              <div class="column">
                <a href="https://voidlinux.org/" target="_blank">
                  <img src="../assets/pictures/Void_Linux_logo.svg" class="logo" alt="Void logo" />
                </a>                
              </div>
            </div>
           
        <p>My opinion on some Linux distros:</p>
        <p>  <span class="colored"><b>Ubuntu : </b></span>  Too much bloat preinstalled. Snap has terrible bloat. Telemetry is probably increasing. Some Ubuntu derivatives don't come with Snap: Bodhi Linux, Pop!_OS and Linux Mint for example. It may change.
        </p>
        <p><span class="colored"><b>Fedora Workstation :</b></span> No minimal installer available. Fedora has a strict policy of including only open source software in its official repositories... but there is a lot of non-free firmware/drivers preinstalled.  Fedora is therefore not FSF-approved. There is also telemetry since Fedora 42.</p>
           <p id="kinoite">Silverblue/Kinoite: minimalistic but it's not suitable for everybody because updates are delivered as full images. That's time consuming and disk space consuming. Flatpak apps are recommended to keep the image small, but Flatpak apps have more issues (bugs and audio or storage permissions problems). Here is a quote from a devs chat: <q>Flatpak doesn’t allow important parts of the Chromium sandbox to work as it should. Chromium browsers and Electron apps distributed on Flathub all rely on a 3rd-party package called Zypak to trick Chromium into thinking its SUID sandbox is present.
          </q></p>
        <p><span class="colored"><b>Manjaro :</b></span> Unsigned packages from time to time. More and more bloat and telemetry.
        </p>
          <p><span class="colored"><b>Debian :</b></span> No bloat but outdated software, especially browsers. No graphical minimal installer, only a CLI installer. Some Debian derivatives have a graphical minimal installer, namely PeppermintOS and Q4OS.
          </p>
          <p id="kinoite">Debian testing: The debian testing branch can move very fast and many users have broken their system. Security patches are not immediately available. The unstable branch is more secure.</p>
            <p><span class="colored"><b>MX Linux :</b></span> Not so bloated. Latest firefox available. For me it's Debian++. Very good distro.
            </p>
            <p><span class="colored"><b>OpenSUSE Tumbleweed :</b></span> Zypper is slower and less reliable than dnf. Many Tumbleweed users have to use Flatpak because OpenSUSE multimedia codec repos are messy and can lead to dependencies issues. Packman repo is maintained by external people who don't follow SUSE policy. Some Packman RPMs might be malicious. 
        </p>
        <p><span class="colored"><b>Arch Linux :</b></span> No bloat. Bleeding edge, so unstability might come from update to update, namely broken glibc and kernel panic at boot. It's generally fixed after 2-3 days. Tip: dual boot Arch with a stable rescue distro to remain operational during these days.   
        </p>
        <p><span class="colored"><b>KaOS :</b></span> No bloat, user-friendly, more stable than Arch Linux. Downside: it's only for KDE users, no kernels choice, limited software choice, not enough mirrors. 
        </p>
        <p><span class="colored"><b>Void Linux:</b></span> No bloat, more stable than Arch Linux. The xbps tools are amazing. Use xbps-src and git to locally install/update packages like Brave browser. Very good distro.
        </p>
        <p><span class="colored"><b>Gentoo :</b></span> Source-based distro, no bloat, more stable than Arch Linux. It takes time to build packages. Better use Gentoo with a window manager like icewm to build quickly. Not suitable for users who need to quickly install big software like libreoffice and chromium.
        </p>
      </div>
     
    </div>
  </template>
  <script>
      export default {
        name: 'Bonus',
        props: {
          msg: String
        }
      }
      </script>
      <!-- Add "scoped" attribute to limit CSS to this component only -->
      <style scoped>
      h3 {
        margin: 40px 0 0;
      }
      ul {
        list-style-type: none;
        padding: 0;
      }
      li {
        display: inline-block;
        margin: 0 10px;
      }
      a {
        color: hsl(305, 11%, 39%);
        font-weight: bold;
      }
      a:hover{
        color: hsl(305, 11%, 28%);
      }
      .colored{
        color: hsl(305, 11%, 37%);
      }
    .centered-marge {            
      /*width: 80%;*/
      /*text-align: center;*/            
    max-width: 650px; /*750 */
   /* position: absolute;*/  
  }
  #article{
    margin-bottom: 200px;
  }
  #kinoite{
    margin-left: 40px;
  }
    
.myrow {
  display: flex;
  justify-content: center;
  align-items: center;
}
.column {
  flex: 50%;
  padding: 5px;
  
}
.logo {
  width: 80%;
  /*height: 6em;*/
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #72b76faa);
}
.padding {
  padding-left: 10px;
}
      </style>