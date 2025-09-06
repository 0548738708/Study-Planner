# Study-Planner
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Study Planner</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --primary: #4361ee;
            --secondary: #3f37c9;
            --success: #4cc9f0;
            --light: #f8f9fa;
            --dark: #212529;
        }
        
        body {
            background-color: #f5f7fb;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        .navbar {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
        }
        
        .sidebar {
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 0 15px rgba(0,0,0,0.1);
            height: calc(100vh - 100px);
            position: sticky;
            top: 20px;
        }
        
        .main-content {
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 0 15px rgba(0,0,0,0.1);
            padding: 25px;
        }
        
        .subject-badge {
            display: inline-block;
            width: 15px;
            height: 15px;
            border-radius: 50%;
            margin-right: 8px;
        }
        
        .calendar-day {
            border: 1px solid #dee2e6;
            height: 120px;
            padding: 8px;
            overflow-y: auto;
        }
        
        .calendar-day.current-day {
            background-color: rgba(67, 97, 238, 0.1);
            border: 2px solid var(--primary);
        }
        
        .session-event {
            font-size: 0.8rem;
            padding: 2px 5px;
            margin-bottom: 3px;
            border-radius: 3px;
            color: white;
        }
        
        .task-item {
            border-left: 4px solid;
            margin-bottom: 10px;
        }
        
        .stats-card {
            border-radius: 10px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 20px;
            margin-bottom: 20px;
        }
    </style>
</head>
<body>
    <!-- Navigation Bar -->
    <nav class="navbar navbar-expand-lg navbar-dark mb-4">
        <div class="container">
            <a class="navbar-brand" href="#">
                <i class="fas fa-graduation-cap me-2"></i>Study Planner
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <a class="nav-link" href="#"><i class="fas fa-home me-1"></i> Dashboard</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#"><i class="fas fa-calendar me-1"></i> Schedule</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#"><i class="fas fa-tasks me-1"></i> Tasks</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#"><i class="fas fa-book me-1"></i> Subjects</a>
                    </li>
                    <li class="nav-item dropdown">
                        <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown">
                            <i class="fas fa-user me-1"></i> John Doe
                        </a>
                        <ul class="dropdown-menu">
                            <li><a class="dropdown-item" href="#">Profile</a></li>
                            <li><a class="dropdown-item" href="#">Settings</a></li>
                            <li><hr class="dropdown-divider"></li>
                            <li><a class="dropdown-item" href="#">Logout</a></li>
                        </ul>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <div class="container">
        <div class="row">
            <!-- Sidebar -->
            <div class="col-lg-3">
                <div class="sidebar p-3 mb-4">
                    <h5 class="mb-3">My Subjects</h5>
                    <ul class="list-group">
                        <li class="list-group-item d-flex align-items-center">
                            <span class="subject-badge" style="background-color: #4361ee;"></span>
                            Mathematics
                        </li>
                        <li class="list-group-item d-flex align-items-center">
                            <span class="subject-badge" style="background-color: #ef476f;"></span>
                            Physics
                        </li>
                        <li class="list-group-item d-flex align-items-center">
                            <span class="subject-badge" style="background-color: #06d6a0;"></span>
                            Chemistry
                        </li>
                        <li class="list-group-item d-flex align-items-center">
                            <span class="subject-badge" style="background-color: #ffd166;"></span>
                            Biology
                        </li>
                    </ul>
                    
                    <h5 class="mt-4 mb-3">Upcoming Tasks</h5>
                    <div class="task-item p-3 bg-light">
                        <div class="d-flex justify-content-between">
                            <strong>Calculus Homework</strong>
                            <span class="badge bg-danger">High</span>
                        </div>
                        <p class="mb-0 small">Chapter 5 exercises</p>
                        <div class="d-flex justify-content-between mt-2">
                            <span class="text-muted"><i class="far fa-clock me-1"></i> Tomorrow</span>
                            <div class="form-check">
                                <input class="form-check-input" type="checkbox">
                            </div>
                        </div>
                    </div>
                    
                    <div class="task-item p-3 bg-light">
                        <div class="d-flex justify-content-between">
                            <strong>Lab Report</strong>
                            <span class="badge bg-warning text-dark">Medium</span>
                        </div>
                        <p class="mb-0 small">Physics experiment</p>
                        <div class="d-flex justify-content-between mt-2">
                            <span class="text-muted"><i class="far fa-clock me-1"></i> 3 days left</span>
                            <div class="form-check">
                                <input class="form-check-input" type="checkbox">
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Main Content -->
            <div class="col-lg-9">
                <div class="main-content mb-4">
                    <div class="d-flex justify-content-between align-items-center mb-4">
                        <h3>Study Dashboard</h3>
                        <button class="btn btn-primary"><i class="fas fa-plus me-1"></i> New Session</button>
                    </div>
                    
                    <!-- Stats Cards -->
                    <div class="row mb-4">
                        <div class="col-md-3">
                            <div class="stats-card">
                                <div class="d-flex justify-content-between align-items-center">
                                    <div>
                                        <h6>Study Sessions</h6>
                                        <h3>12</h3>
                                        <p class="mb-0">This week</p>
                                    </div>
                                    <i class="fas fa-calendar-alt fa-2x"></i>
                                </div>
                            </div>
                        </div>
                        <div class="col-md-3">
                            <div class="stats-card" style="background: linear-gradient(135deg, #ef476f, #f15a80);">
                                <div class="d-flex justify-content-between align-items-center">
                                    <div>
                                        <h6>Pending Tasks</h6>
                                        <h3>7</h3>
                                        <p class="mb-0">To complete</p>
                                    </div>
                                    <i class="fas fa-tasks fa-2x"></i>
                                </div>
                            </div>
                        </div>
                        <div class="col-md-3">
                            <div class="stats-card" style="background: linear-gradient(135deg, #06d6a0, #08c290);">
                                <div class="d-flex justify-content-between align-items-center">
                                    <div>
                                        <h6>Completed</h6>
                                        <h3>24</h3>
                                        <p class="mb-0">This month</p>
                                    </div>
                                    <i class="fas fa-check-circle fa-2x"></i>
                                </div>
                            </div>
                        </div>
                        <div class="col-md-3">
                            <div class="stats-card" style="background: linear-gradient(135deg, #ffd166, #ffb74d);">
                                <div class="d-flex justify-content-between align-items-center">
                                    <div>
                                        <h6>Study Hours</h6>
                                        <h3>36</h3>
                                        <p class="mb-0">This month</p>
                                    </div>
                                    <i class="fas fa-clock fa-2x"></i>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Calendar View -->
                    <h5 class="mb-3">Weekly Schedule</h5>
                    <div class="table-responsive mb-4">
                        <table class="table table-bordered">
                            <thead>
                                <tr>
                                    <th scope="col">Monday</th>
                                    <th scope="col">Tuesday</th>
                                    <th scope="col">Wednesday</th>
                                    <th scope="col">Thursday</th>
                                    <th scope="col">Friday</th>
                                    <th scope="col">Saturday</th>
                                    <th scope="col">Sunday</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr>
                                    <td class="calendar-day">
                                        <div class="fw-bold">15</div>
                                        <div class="session-event" style="background-color: #4361ee;">Math: 9:00-10:30</div>
                                        <div class="session-event" style="background-color: #06d6a0;">Chemistry: 14:00-15:30</div>
                                    </td>
                                    <td class="calendar-day">
                                        <div class="fw-bold">16</div>
                                        <div class="session-event" style="background-color: #ef476f;">Physics: 10:00-11:30</div>
                                    </td>
                                    <td class="calendar-day">
                                        <div class="fw-bold">17</div>
                                        <div class="session-event" style="background-color: #ffd166;">Biology: 11:00-12:30</div>
                                        <div class="session-event" style="background-color: #4361ee;">Math: 15:00-16:30</div>
                                    </td>
                                    <td class="calendar-day current-day">
                                        <div class="fw-bold">18</div>
                                        <div class="session-event" style="background-color: #ef476f;">Physics: 9:30-11:00</div>
                                        <div class="session-event" style="background-color: #06d6a0;">Chemistry: 16:00-17:30</div>
                                    </td>
                                    <td class="calendar-day">
                                        <div class="fw-bold">19</div>
                                        <div class="session-event" style="background-color: #4361ee;">Math: 10:00-11:30</div>
                                    </td>
                                    <td class="calendar-day">
                                        <div class="fw-bold">20</div>
                                        <div class="session-event" style="background-color: #ffd166;">Biology: 13:00-14:30</div>
                                    </td>
                                    <td class="calendar-day">
                                        <div class="fw-bold">21</div>
                                        <div class="session-event" style="background-color: #06d6a0;">Chemistry: 15:00-16:30</div>
                                    </td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                    
                    <!-- Today's Sessions -->
                    <h5 class="mb-3">Today's Study Sessions</h5>
                    <div class="row">
                        <div class="col-md-6 mb-3">
                            <div class="card">
                                <div class="card-body">
                                    <div class="d-flex justify-content-between">
                                        <h5 class="card-title">Physics Review</h5>
                                        <span class="badge bg-primary">9:30 - 11:00</span>
                                    </div>
                                    <p class="card-text">Chapter 7: Thermodynamics</p>
                                    <div class="d-flex justify-content-between align-items-center">
                                        <span class="text-muted"><i class="fas fa-book me-1"></i> Physics</span>
                                        <div>
                                            <button class="btn btn-sm btn-outline-primary me-1"><i class="fas fa-edit"></i></button>
                                            <button class="btn btn-sm btn-outline-danger"><i class="fas fa-trash"></i></button>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="col-md-6 mb-3">
                            <div class="card">
                                <div class="card-body">
                                    <div class="d-flex justify-content-between">
                                        <h5 class="card-title">Chemistry Lab</h5>
                                        <span class="badge bg-success">16:00 - 17:30</span>
                                    </div>
                                    <p class="card-text">Experiment #5: Reaction Rates</p>
                                    <div class="d-flex justify-content-between align-items-center">
                                        <span class="text-muted"><i class="fas fa-book me-1"></i> Chemistry</span>
                                        <div>
                                            <button class="btn btn-sm btn-outline-primary me-1"><i class="fas fa-edit"></i></button>
                                            <button class="btn btn-sm btn-outline-danger"><i class="fas fa-trash"></i></button>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
