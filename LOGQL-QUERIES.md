# LogQL Queries - WordPress Product

## Query 1 - Toan bo log Nginx
{container="wp_nginx"}

## Query 2 - Loc cac HTTP GET request
{container="wp_nginx"} |= "GET"

## Query 3 - Loc cac loi HTTP 404
{container="wp_nginx"} |= "404"
