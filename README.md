# Это просто кусок кода
```
data class Commit(
    val tree: Tree,
    val previousCommit: Commit?
)

interface SnapshotPart

data class Tree(
    val tree: Map<String, SnapshotPart>
) : SnapshotPart

data class Blob(
    val content: List<Byte>
) : SnapshotPart
```