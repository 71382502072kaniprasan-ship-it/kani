# kani
Employee Payroll Naming Convention Improvement
```jsx
import { useNavigate } from "react-router-dom";
import authService from "../services/authService";

function Navbar() {
  const navigate = useNavigate();
  const user = authService.getCurrentUser();

  const handleLogout = () => {
    authService.logout();
    navigate("/login");
  };

  return (
    <header className="navbar">
      <h2>Employee Payroll System</h2>

      <div className="navbar-right">
        <span>
          Welcome, {user?.username || "User"}
        </span>

        <button onClick={handleLogout}>
          Logout
        </button>
      </div>
    </header>
  );
}

export default Navbar;
```
