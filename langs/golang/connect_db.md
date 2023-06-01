## golang postgres

postgre не працює з placeholder формат ?,?

лише через $1,$2

```golang
import (
	"database/sql"
	_ "github.com/lib/pq"
)

// ...

db, err := sql.Open("postgres", "postgres://username:password@localhost/db_name?sslmode=disable")
```
