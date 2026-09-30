var description = fd_data.trigger.current.description.toLowerCase();

var category = "General";
var priority = "Low";

if (
    description.includes("password") ||
    description.includes("login") ||
    description.includes("account")
) {
    category = "Access / Account";
    priority = "Medium";
}
else if (
    description.includes("computer") ||
    description.includes("laptop") ||
    description.includes("desktop") ||
    description.includes("system")
) {
    category = "Hardware";
    priority = "Medium";
}
else if (
    description.includes("software") ||
    description.includes("application") ||
    description.includes("app") ||
    description.includes("install")
) {
    category = "Software";
    priority = "Medium";
}
else if (
    description.includes("network") ||
    description.includes("internet") ||
    description.includes("wifi")
) {
    category = "Network";
    priority = "High";
}
else if (
    description.includes("server") ||
    description.includes("database") ||
    description.includes("down")
) {
    category = "Server / Database";
    priority = "High";
}
else if (
    description.includes("urgent") ||
    description.includes("critical")
) {
    category = "Critical Issue";
    priority = "Critical";
}

return {
    category: category,
    priority: priority
};
