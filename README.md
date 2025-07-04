# easyeffects-collection
A collection of easyeffects presets meant for laptops, but may work with headphones too.

# About

This repository, contains a collection of json config files, meant to be used with easyeffects, to enhance audio on laptop speakers.

On Linux, based on my experience, PipeWire default settings output the RAW audio, making it sound like cheap audio, compared to Windows. the files here aim to fix that. 

This also contains files that can be used when using headphones and regular speakers.

IRS files are also provided, to be used with the convolver.

## Linux Requirements:
Easyeffects and pipewire should be already properly configured. 

On Arch Linux it can be installed with:
`sudo pacman -S calf lsp-plugins-lv2 zam-plugins-lv2 mda.lv2 yelp easyeffects`

Refer to your distro package manager to know the equivalent for eg, Linux Mint/Fedora.

Most distros ship pipewire by default, as it's the recommended audio stack nowadays.

## Windows Requirements:

### In case you don't have Windows installed, you can use Windows to Go, by creating it with Rufus. If you're dual booting, you can skip this step, and just boot into Windows.

Boot into windows, and look for the following settings:

![samplerate2](https://github.com/user-attachments/assets/3fe228f1-acce-48e2-b9b8-bb1af2d2610c)
![samplerate](https://github.com/user-attachments/assets/06f1acdc-3a5a-44fd-b4b6-8d7153cb5578)

In my case, my audio card only supports 48KHz, 16 bit samplerate. 

So, you may configure pipewire.conf like this:

![image](https://github.com/user-attachments/assets/cf2da13e-658a-495d-ad02-e3b4d4e064a3)

You need to adjust it to match your soundcard specifications.
### While on Windows, play some music, and if possible, record the audio output from your laptop speakers with a good mic. This is to have a reference audio, so you can find the right profile that matches the same audio experience.
# Reference docs:

This post can help to calculate the right values:

https://www.reddit.com/r/linux_gaming/comments/1gao420/low_latency_guide_for_linux_using_pipewire/

Official docs can be found here:

https://docs.pipewire.org/page_man_pipewire_1.html

Another useful post regarding values:

https://bbs.archlinux.org/viewtopic.php?id=288886

For a more in depth documentation:
https://wiki.gentoo.org/wiki/PipeWire/en#Configuration_fragments

Once done, proceed to use the config files.
Be sure that pipewire.conf, client.conf and pipewire-pulse.conf have the right quantum, and match the samplerate that windows uses for your audio card. 

## How to use:

`git clone` this repo, and place the files on `~/.config/easyeffects` or on `~/.var/app/com.github.wwmm.easyeffects/config/easyeffects/output/` if using the flatpak version.

Then, open EasyEffects, and open the profiles drop down. start testing the profiles and adjust them to your needs.
