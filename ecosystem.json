{
    "apps": [
        {
            "name": "test",
            "script": "server.js",
            "env": {
                "COMMON_VARIABLE": "true"
            },
            "env_production": {
                "NODE_ENV": "production"
            }
        }
    ],
    "deploy": {
        "production": {
            "key": "/Users/goncalo/Documents/keys/goncalo.pem",
            "user": "ec2-user",
            "host": "54.72.71.37",
            "ref": "origin/master",
            "repo": "https://github.com/DevAlien/node-js-sample.git",
            "path": "~/test",
            "post-deploy": "pm2 startOrRestart ecosystem.json --env production"
        },
        "dev": {
            "user": "node",
            "host": "212.83.163.1",
            "ref": "origin/master",
            "repo": "git@github.com:repo.git",
            "path": "/var/www/development",
            "post-deploy": "pm2 startOrRestart ecosystem.json --env dev"
        }
    }
}
