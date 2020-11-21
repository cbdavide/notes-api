# Notes API

It is a repository of notes where you can query your notes by tags or
by words contained in the notes.

## Endpoints draft

`[POST] api/note`

```
{
    tags: [str],
    content: str
}
```

`[GET] api/notes`

Query string parameters:

- tags: list[str] -- Get all the notes that have that tag.
- text: str -- Get all the notes whose content matches the given text.

## Persistence

### Notes

The notes are going to be stored in elasticsearch documents.

```
{
    token: str,
    tags: [str],
    content: str,
    user_token: str,
    created_at: str,
    updated_at: str,
    read_permission: [str],
    write_permission: [str],
}
```

### Users

The users are going to be stored in a relational database.


