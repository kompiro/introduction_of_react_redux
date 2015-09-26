!SLIDE
# What is React.js? #

- JUST THE UI (only View FW)
- VIRTUAL DOM (abstruction and performance)
- DATA FLOW (simple)

- Developed by facebook

!SLIDE code small

# JUST THE UI #

    @@@javascript
    import React, {Component} from 'React';

    class HelloMessage extends Component {
      render() {
        return <div>Hello {this.props.name}</div>;
      }
    });

    React.render(<HelloMessage name="John" />, mountNode);

write `<HelloMessage />`: abstraction (includes css and js deps.)

!SLIDE code small

# VIRTUAL DOM #

    @@@xml

    <ul className="nav nav-pills nav-stacked">
      {commits.map((commit)=>
        <li className={currentId === commit.id ? 'active' : ''}>
        <Link to={`/commits/${commit.id}`}>
          {commit.shortMessage}
        </Link>
        </li>
      )}
    </ul>

!SLIDE

# DATA FLOW #

- one-way reactive data flow
- **Redux** takes the responsibility

!SLIDE

# What is Redux? #

The application state tree is...

- Single source
- Immutable (read-only)
- Changed by pure function

!SLIDE
# 4 Basic Concept #

- Store
  - store state and action dispatcher
- Action Creator
  - called from UI
- Action
  -  change state (object)
- Reducer
  - change state (pure function)

!SLIDE
# Interesting Point #

- [see all application state](https://github.com/gaearon/redux-devtools#redux-devtools)
- Timetravel mode (Undo/Redo)
