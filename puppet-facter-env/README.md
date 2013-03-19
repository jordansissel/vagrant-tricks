# Facter, Puppet, Vagrant.

Goal: Set FACTER environment variables in `vagrant up` and `vagrant provision` and
have them passed into the puppet provisioning.

Example run:

    % FACTER_greeting="Hello, world." vagrant up
    Bringing machine 'default' up with 'virtualbox' provider...
    ...
    [default] Running provisioner: VagrantPlugins::Puppet::Provisioner::Puppet...
    Running Puppet with site.pp...
    stdin: is not a tty
    Warning: Could not retrieve fact fqdn
    Notice: Scope(Class[main]): Facter says Hello, world.
    Notice: Finished catalog run in 0.09 seconds

See the `Vagrantfile` in this repo for a fully-working example.
