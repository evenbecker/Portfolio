<template>
    <div class="centered-fixed">
      <div id="article">
        <h4 class="verdanaH">Linux as a desktop OS</h4>                  
        <p> Linux works nice on server, but on desktop, there are more things to consider: multimedia codecs, Wi-Fi drivers, GPU drivers, CPU microcode, printers drivers, ... Problems may happen. Never expect popular distros to make things working out-of-the-box as they pretend to do. Better learn the CLI and read the <a href="https://wiki.archlinux.org/title/Main_page">Arch wiki</a>. A good Linux user doesn't need GUI tools besides the installer.<br> Opinions about bloat are divided. <a href="https://www.gnu.org/distros/free-distros.en.html">FSF-approved</a> Trisquel GNU/Linux gives a good idea about what to avoid. Trisquel doesn't have a Gnome edition, so I don't use Gnome.</p>
        <p>My opinion on some Linux distros:</p>
        <p>  <b>Ubuntu : </b>  Too much bloat preinstalled. Snap has terrible bloat. Telemetry is probably increasing. Some Ubuntu derivatives don't come with Snap: Bodhi Linux, Pop!_OS and Linux Mint for example. It may change.
        </p>
        <p><b>Fedora Workstation :</b> It seems lean at first glance... but there are +700 MB of non-free firmware/drivers preinstalled. No minimal installer. Thus, according to the FSF, Fedora is bloated. There is also telemetry since Fedora 42. Silverblue/Kinoite is minimalistic but it's not suitable for everybody because updates are delivered as full images. That's time consuming and disk space consuming.
        </p>
        <p><b>Manjaro :</b> Unsigned packages from time to time. More and more bloat and telemetry.
        </p>
          <p><b>Debian :</b> No bloat but outdated software, especially browsers. No graphical minimal installer, only a CLI installer. Some Debian derivatives have a graphical minimal installer, namely PeppermintOS and Q4OS.
          </p>
            <p><b>MX Linux :</b> Not so bloated. Latest firefox available. For me it's Debian++. Very good distro.
            </p>
            <p><b>OpenSUSE Tumbleweed :</b> Zypper is slower and less reliable than dnf. Many Tumbleweed users have to use Flatpak because OpenSUSE multimedia codec repos are messy and can lead to dependencies issues. Packman repo is maintained by external people who don't follow SUSE policy. Some Packman RPMs might be malicious. 
        </p>
        <p><b>Arch Linux :</b> No bloat. Bleeding edge, so unstability might come from update to update, namely broken glibc and kernel panic at boot. It's generally fixed after 2-3 days. Tip: dual boot Arch with a stable rescue distro to remain operational during these days.   
        </p>
        <p><b>KaOS :</b> No bloat, user-friendly, more stable than Arch Linux. Downside: it's only for KDE users, no kernels choice, limited software choice, not enough mirrors. 
        </p>
        <p><b>Void Linux:</b> No bloat, more stable than Arch Linux. The xbps tools are amazing. Use xbps-src and git to locally install/update packages like Brave browser. Very good distro.
        </p>
        <p><b>Gentoo :</b> Source-based distro, no bloat, more stable than Arch Linux. It takes time to build packages. Better use Gentoo with a window manager like icewm to build quickly. Not suitable for users who need to quickly install big software like libreoffice and chromium.
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
        color: #6f596d;
      }
    .centered-fixed {
      /*position: fixed;
      z-index:1;
      top: 0;*/
      
      /*width: 80%;*/
      /*text-align: center;*/
      min-width: 510px;
    max-width: 750px; 
    position: absolute;

  left: 50%;
  transform: translate(-50%, 0);
  }
  #article{
    margin-bottom: 200px;
  }
      .white {
        background-color: white;
        left: 0;
        width:100%;
        text-align: center;
      }
      </style>