= struct =
Collection of fields


type Vertex struct {
  X int
  Y int
}

func main() {
  fmt.Println(Vertex{1, 2})
}

# Struct literals
var (
  v1 = Vertex{1, 2}
  v2 = Vertex{X:1}
  v3 = Vertex{}
  p = &Vertex{1, 2}
)

# Accessing through poiter
v := Vertext{1,2}
p := &v
p.X = 20
