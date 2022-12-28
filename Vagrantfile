Vagrant.configure("2") do |config|
  config.vm.provision "shell", inline: "echo Hello"

  config.vm.define "ansible" do |ansible|
    ansible.vm.box = "ubuntu/focal64"
    ansible.vm.network "public_network", ip: "192.168.1.100"
    ansible.vm.box_download_insecure = true
    ansible.vm.provision "shell", inline: <<-SHELL
    sed -i 's/PasswordAuthentication no/PasswordAuthentication yes/g' /etc/ssh/sshd_config    
    systemctl restart sshd.service
    SHELL
  end

  config.vm.define "linux1" do |linux1|
    linux1.vm.box = "ubuntu/focal64"
    linux1.vm.network "public_network", ip: "192.168.1.101"
    linux1.vm.box_download_insecure = true
    linux1.vm.provision "shell", inline: <<-SHELL
    sed -i 's/PasswordAuthentication no/PasswordAuthentication yes/g' /etc/ssh/sshd_config    
    systemctl restart sshd.service
  SHELL
  end

  config.vm.define "linux2" do |linux2|
    linux2.vm.box = "ubuntu/focal64"
    linux2.vm.network "public_network", ip: "192.168.1.102"
    linux2.vm.box_download_insecure = true
    linux2.vm.provision "shell", inline: <<-SHELL
    sed -i 's/PasswordAuthentication no/PasswordAuthentication yes/g' /etc/ssh/sshd_config    
    systemctl restart sshd.service
  SHELL
  end
  
  config.vm.define "linux3" do |linux3|
    linux3.vm.box = "ubuntu/focal64"
    linux3.vm.network "public_network", ip: "192.168.1.103"
    linux3.vm.box_download_insecure = true
    linux3.vm.provision "shell", inline: <<-SHELL
    sed -i 's/PasswordAuthentication no/PasswordAuthentication yes/g' /etc/ssh/sshd_config    
    systemctl restart sshd.service
  SHELL
  end
   
end