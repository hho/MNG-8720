# Reproducer for MNG-8720

Note the symlink `foo`
    
* Run `mvn validate` (or similar) in `projects/clientA/foo/bar` (= full path)    
  ➡️ no warning message is produced

* Run same command from `foo/bar` (= symlinked path)    
  ➡️ warning `Project root directory and multiModuleProjectDirectory are not aligned` in the output

Tested with Maven 4.0.0-rc-3
