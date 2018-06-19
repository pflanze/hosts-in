# Generate /etc/hosts

## Installation

The `verify-sig` commands assume that you already installed [git-sign](https://github.com/pflanze/git-sign); if you don't want to verify code integrity, ignore those.

	cd /opt/chj
	git clone https://github.com/pflanze/ssh-config-gen.git
	( cd ssh-config-gen && verify-sig v2 )
	git clone https://github.com/pflanze/hosts-in.git
	( cd hosts-in && verify-sig v1 )

The `concentrate` program is already linked from chj-bin, hence
reachable if you use the latter. If you don't, add
`/opt/chj/hosts-in/bin` to your `PATH`.


## Usage

Run `concentrate start` to regenerate `/etc/hosts` when wanting to
concentrate, `concentrate stop` otherwise.

Note: [chj-bin](https://github.com/pflanze/chj-bin) also contains
`astart` and `astop` wrappers to make the above commands shorter.

## TODO

Generate anti-track entries programmatically via enumeration and
remote APIs. Or look into other tools.
