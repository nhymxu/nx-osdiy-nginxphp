# nhymxu/nx-osdiy-nginxphp
This is a sample repository to get nginx + php fpm running on openshift.
Based on idea from boekkooi.

More information about openshift: https://openshift.redhat.com/

## What's inside

**The `.openshift/action_hooks` scripts:**

* start
    - Starts Nginx and php-fpm
* stop
    - Stops Nginx and php-fpm

**The `.openshift/tmpl` templates:**

Here are the templates used by the build and deploy scripts.
Just customize away.

**The `public/` nginx web folder:**

The web folder currently used. You can change this in `.openshift/tmpl/nginx.conf.tmpl`.

## Usage

To get PHP 7 working at OpenShift, you have to do the following:

1. Create a new Openshift "Do-It-Yourself" application
2. SSH into your gear and Run command "gear stop"
3. Clone this repository and Put file in correct folder 
4. Run command "cd ${OPENSHIFT_REPO_DIR}/.openshift"
5. Run command "chmod +x nx" and "chmod +x nx_deploy"
6. Run command "sh nx"
7. Wait for build to finish (This may take at least an hour)
8. Run command "sh nx_deploy"
9. Run command "gear restart"
 
## Extra's