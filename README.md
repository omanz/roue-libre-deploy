# roue-libre-deploy

docker-compose for server deployment.
For first deployment, store init.sql from blog in an accessible path for docker-compose maria db (./blog)
Don't forget Caddyfile
´´´
my-domain.com {
        reverse_proxy blog:8080
}
other.my-domain.com {
        reverse_proxy upload_tool:8081
}
´´´
Don't forget env file:
´´´
DB_PASS="db_pass"
DB_USER="db_user"
DB_HOST=dbhost
BLOG_AUTH_PASSWORD=blog_auth_password
BLOG_AUTH_USERNAME=blog_auth_username
BLOG_HOST=blog_host:port
PUBLIC_PHOTOS_PATH=/my/path/
TPM_PHOTOS_PATH=/tmp/path/
UPLOAD_TOOL_AUTH_PASSWORD=upload_tool_auth_password
UPLOAD_TOOL_AUTH_USERNAME=upload_tool_auth_username
´´´
