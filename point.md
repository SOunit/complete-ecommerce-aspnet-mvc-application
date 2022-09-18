# Model

- database table

# DbContext

- translate Model and Database
- inherit `DbContext` class from ASP.NET package

- need SQL server connection info
- add to services

# setup table relationship

- edit `Model` class, add foreign key and etc.
- add `Model_Model` class to `many-to-many` relationship
- edit `DbContext`
  - setup relationship
  - add table name

# Task

- Task is for async

```
public async Task<IActionResult> Index()
{
    var allProducers = await _context.Producers.ToListAsync();
    return View(allProducers);
}
```
