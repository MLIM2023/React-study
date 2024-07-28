```jsx
import PropTypes from 'prop-types'

function Student(props) {
    return (
        <div className="student">
            <p>Name:{props.name}</p>
            <p>Age:{props.age}</p>
            <p>Student:{props.isStudent ? "Yes" : "No"}</p>
        </div>
    );

}
//类似于严格模式，要求键入的属性必须与之相应，程序会照常运行，只是会在控制台显示错误 
Student.propTypes = {
    name: PropTypes.string,
    age: PropTypes.number,
    isStudent: PropTypes.bool,
}
//如果不输入则默认自动键入
Student.defaultProps = {
    name: "Guest",
    age: 0,
    isStudent: false,
}

export default Student
```